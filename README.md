# String encoding conversions in Julia using iconv

[![Build Status](https://travis-ci.com/AStupidBear/Iconv.jl.svg?branch=master)](https://travis-ci.com/AStupidBear/Iconv.jl)
[![Build Status](https://ci.appveyor.com/api/projects/status/github/AStupidBear/Iconv.jl?svg=true)](https://ci.appveyor.com/project/AStupidBear/Iconv-jl)
[![Coverage](https://codecov.io/gh/AStupidBear/Iconv.jl/branch/master/graph/badge.svg)](https://codecov.io/gh/AStupidBear/Iconv.jl)

## Installation

Make sure `iconv` is installed on your system, then

```julia
using Pkg
pkg"add Iconv"
```

On Windows, you can install `iconv` using [Scoop](https://scoop.sh/) 

```
scoop install iconv
```

## Usage

```julia
iconv("笨熊", "UTF-8", "GBK") == togbk("笨熊") == g"笨熊"
iconv(g"笨熊", "GBK", "UTF-8") == toutf8(g"笨熊") == b"笨熊"
```
