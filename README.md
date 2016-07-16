# goow

goow is a basic web scraper for the Overwatch stats site. It can be seen as a premature API binding for the Overwatch API written in Go.

### Installing

```
go get github.com/sdwolfe32/goow
```

### Usage

All that's needed to get player stats is to pass the {platform}, {region}, and {tag} to the GetPlayerStats() func. For example:

```
player, _ := goow.GetPlayerStats("pc", "us", "Viz-1213")
```
The above example should return to you a PlayerStats struct containing detailed statistics for the specified Overwatch player.

## Full example

```
package main

import (
	"log"

	"github.com/sdwolfe32/goow"
)

func main() {
	log.Println(goow.GetPlayerStats("pc", "us", "Viz-1213"))
}
```

## Disclaimer
goriot isn’t endorsed by Blizzard and doesn’t reflect the views or opinions of Blizzard or anyone officially involved in producing or managing Overwatch. Overwatch and Blizzard  are trademarks or registered trademarks of Blizzard Entertainment, Inc. Overwatch © Blizzard Entertainment, Inc.

The MIT License (MIT)
=====================

Copyright © 2016 Steven Wolfe

Permission is hereby granted, free of charge, to any person
obtaining a copy of this software and associated documentation
files (the “Software”), to deal in the Software without
restriction, including without limitation the rights to use,
copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following
conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.
