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
