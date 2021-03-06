# Elm Plot

Plot stuff in svg with Elm!

[![Build Status](https://travis-ci.org/terezka/elm-plot.svg?branch=master)](https://travis-ci.org/terezka/elm-plot)

![alt tag](https://raw.githubusercontent.com/terezka/elm-plot/master/example.png)

## Overview

Currently, this library can draw line and area series, grids, axis' with easily configurable ticks and labels.

### What does the api look like?

```elm
    main =
		plot
			[ size plotSize
			, margin ( 10, 20, 40, 20 )
			]
			[ line
			    [ Line.stroke pinkStroke
			    , Line.strokeWidth 2
			    ]
			    data
			, xAxis
			    [ Axis.line [ Line.stroke axisColor ]
			    , Axis.tick [ Tick.viewDynamic toTickStyle ]
			    , Axis.label [ Label.viewDynamic toLabelStyle ]
			    ]
			]
```

### You need something?

Let me know! Open an issue (or PR) or write at #elm-plot in the elm-lang's [slack](http://elmlang.herokuapp.com). I focus on meeting my own needs as well as to that of the community, so please don't hesistate! ✨
## Development

### Setup

```elm
elm package install
```

### Run

```
elm-reactor
```

and open [example](http://localhost:8000/examples/PlotExample.elm)

### Compile the Docs

```
elm-make docs/Docs.elm --output=docs/docs.js
```

### Tests

Tests are written with [elm-test](https://github.com/elm-community/elm-test).
For further information on elm-test check the documentation.
All required dependencies are downloaded and installed when initially running the command.

```
elm-test
```
