# tutorial

following: https://packaging.python.org/en/latest/tutorials/packaging-projects/

## create

```bash
poetry new --name example_package_kimcharli --src py_packaging_tutorial 
```


## build

```bash
poetry build
```

## test build (need clarification)
```
poetry source add --priority=supplemental test https://pypi.example.org/simple/
poetry config repositories.test-pypi https://test.pypi.org/legacy/
poetry config repositories.example_package_kimcharli  https://test.pypi.org/legacy/
poetry config pypi-token.example_package_kimcharli pypi-AgEN...dNHx
```


```
poetry publish --build --repository example_package_kimcharli
```

## test install


```
python3 -m venv ~/venv/test
source ~/venv/test/bin/activate
pip install --index-url https://test.pypi.org/simple/ --no-deps example-package-kimcharli
pip show example-package-kimcharli 
```

```
(test) ckim@ckim-mbp Projects % python                             
Python 3.11.4 (main, Jul 25 2023, 17:07:07) [Clang 14.0.3 (clang-1403.0.22.14.1)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> from example_package_kimcharli.example import add_one
>>> add_one(2)
3
>>> ^D
(test) ckim@ckim-mbp Projects % 
```
