# 3dbinpacking

A Golang 3D Bin Packing Implementation

## Install

```bash
go get github.com/custom-app/binpacking
```

## Usage
```go
package main

import "github.com/custom-app/binpacking"

type goods [4]int

func (g goods) GetWidth() int {
	return g[0]
}

func (g goods) GetHeight() int {
	return g[1]
}

func (g goods) GetDepth() int {
	return g[2]
}

func (g goods) GetWeight() int {
	return g[3]
}

func main() {
	// pass empty slice to use BoxSamples
	packer := binpacking.NewPacker([]binpacking.Box{
		{Width: 260, Height: 120, Depth: 170, Weight: 110, Name: "Box1"},
	})
	packer.Pack([]binpacking.Item{goods([4]int{100, 100, 100, 10}))
}
```
