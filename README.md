ghr [![wercker status](https://app.wercker.com/status/d03e68731c944d8202914a8aaa93d3f0/s "wercker status")](https://app.wercker.com/project/bykey/d03e68731c944d8202914a8aaa93d3f0)
====

Easy to release your packages to Github Release page.

## Description

`ghr` enable you to create Github release page and upload your artifacts to it. `ghr` will parallelize upload multiple artifacts.

## Demo

![](http://deeeet.com/writing/images/post/ghr.gif)

Result is [here](https://github.com/tcnksm/ghr/releases/tag/v0.1.0).

## VS.

- [aktau/github-release](https://github.com/aktau/github-release) - `github-release` can also create and edit releases and upload artifacts. It has many options. `ghr` is a simple alternative. And `ghr` will parallelize upload artifacts.


## Usage

Run it in your project directory:

```bash
$ ghr [option] <tag> <artifacts>
```

You need to set `GITHUB_TOKEN` environmental variable:

```bash
$ export GITHUB_TOKEN="....."
```

## Example

To upload all package in `pkg` directory with tag `v0.1.0`

```bash
$ ghr v0.1.0 pkg/
--> Uploading: pkg/0.1.0_SHASUMS
--> Uploading: pkg/ghr_0.1.0_darwin_386.zip
--> Uploading: pkg/ghr_0.1.0_darwin_amd64.zip
--> Uploading: pkg/ghr_0.1.0_linux_386.zip
--> Uploading: pkg/ghr_0.1.0_linux_amd64.zip
--> Uploading: pkg/ghr_0.1.0_windows_386.zip
--> Uploading: pkg/ghr_0.1.0_windows_amd64.zip
```

## Install

If you are OSX user, you can use [Homebrew](http://brew.sh/):

```bash
$ brew tap tcnksm/ghr
$ brew install ghr
```

If you are in another platform, download binary from [relase page](https://github.com/tcnksm/ghr/releases) and place it in `$PATH` directory. 

## Contribution

1. Fork ([https://github.com/tcnksm/ghr/fork](https://github.com/tcnksm/ghr/fork))
1. Create a feature branch
1. Commit your changes
1. Rebase your local changes against the master branch
1. Run test suite with the `make test` command and confirm that it passes
1. Run `gofmt -s`
1. Create new Pull Request

You can get source with `go get`:

```bash
$ go get -d github.com/tcnksm/ghr
$ cd $GOPATH/src/github.com/tcnksm/cli-init
$ make install
```

## Licence

[MIT](https://github.com/tcnksm/ghr/blob/master/LICENCE)

## Author

[tcnksm](https://github.com/tcnksm)
