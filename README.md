# codenames

[![GoDoc](https://godoc.org/github.com/jbowens/codenames?status.svg)](https://godoc.org/github.com/jbowens/codenames)

Codenames implements a web app for generating and displaying boards for the <a href="https://en.wikipedia.org/wiki/Codenames_(board_game)">Codenames</a> board game. Generated boards are shareable and will update as words are revealed. The board can be viewed either as a spymaster or an ordinary player.

A hosted version of the app is available at [www.horsepaste.com](https://www.horsepaste.com).

![Spymaster view of board](https://raw.githubusercontent.com/jbowens/codenames/master/screenshot.png)

## Building

The app requires a [Go](https://golang.org/) toolchain, node.js and [parcel](https://parceljs.org/) to build. Once you have those setup, build the application Go binary with:

```
go install github.com/jbowens/codenames/cmd/codenames
```

Then from the frontend directory, install the node modules:

```
npm install
```

and start the app (listens to changes)

```
npm start
```

or build the app

```
npm run build
```

### Docker

Alternatively, the reposotiry includes a Dockerfile for building a docker image of this app.

```
docker build . -t codenames:latest
```

The following command will launch the docker image:

```
docker run -p 80:80 codenames
```

Stop the container with `^C`
