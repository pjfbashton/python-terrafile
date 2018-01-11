# python-terrafile

Manages external Terraform modules, controlled by a `Terrafile`.

This is basically a Python version of the tool described at [http://bensnape.com/2016/01/14/terraform-design-patterns-the-terrafile/](http://bensnape.com/2016/01/14/terraform-design-patterns-the-terrafile/)

It also supports Terraform Registry. All you need to do is prepend module path with `tfr::` in your Terrafile.

```shell
tf-aws-lambda:
  source: "tfr::/claranet/lambda/aws"
  version: "v0.1.0"
```

## Installation

```shell
pip install terrafile
```

## Usage

```shell
pterrafile [path]
```

If `path` is provided, it must be the path to a `Terrafile` file, or a directory containing one. If not provided, it looks for the file in the current working directory.
