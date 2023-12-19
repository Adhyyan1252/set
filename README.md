# Set Game Repository
This repository contains the code for a web-based implementation of the Set card game. It includes all necessary assets and scripts to deploy and run the game in a web environment. The live version of the game can be played at [set.stevenhao.com](http://set.stevenhao.com).
## Introduction

The Set card game is a real-time puzzle where players identify patterns among cards with different symbols, colors, and numbers. This repository hosts the code that runs a digital version of the game, allowing players to enjoy Set in a browser.

## Game Description

Set is a compelling card game that challenges players to identify patterns among a grid of cards, each adorned with symbols, shading patterns, and colors. The deck consists of 81 unique cards, and at the start of the game, 12 cards are laid out in a grid. Players must be swift and observant, aiming to locate a "set" of three cards where each attribute—number of symbols (one, two, or three), type of symbols (oval, squiggle, or diamond), shading (solid, striped, or open), and color (red, green, or purple)—is either all the same or all different across the cards. The game progresses as players continue to identify sets, and new cards are dealt from the deck to replace them, offering a dynamic and continuously engaging experience.

## File Structure

The repository's structure is as follows:

- `public/`: Contains the HTML, CSS, CoffeeScript, and JavaScript files necessary for the game's frontend.
  - `index.html`: The main entry point for the game.
  - `*.coffee`: CoffeeScript files that define game logic.
  - `*.js`: JavaScript files for additional functionality.
  - `*.css`: Style sheets for the game's appearance.
  - `*.png`, `*.ico`: Image assets used in the game.
- `README.md`: The file you are currently reading.
- `deploy.sh`: A script for deploying the game to a production environment.
- `dev.sh`: A script for deploying the game to a development environment.

## How to Play

To dive into the game, navigate to [set.stevenhao.com](http://set.stevenhao.com) where you'll be greeted with the option to start a new game. No account creation is necessary—simply click to begin. The game interface presents a grid of cards, and you can select a set by clicking on three cards that meet the criteria of a set. If your selection is correct, the cards will be removed and replaced with new ones from the deck. If incorrect, the game will prompt you to try again. Keep an eye on the timer, as speed is essential! Your goal is to find as many sets as possible before the deck is depleted, with your final score reflecting the number of sets you've successfully identified.

## How to Build

The game's frontend is built with CoffeeScript and JavaScript. If you want to make changes to the CoffeeScript files, you will need to compile them to JavaScript. This requires a CoffeeScript compiler, which can be installed and run as follows:

```sh
npm install -g coffee-script
coffee -c public/*.coffee
```

## How to Deploy

To deploy the game to your server, you can use the provided `deploy.sh` script, which requires `rsync`. Update the script with your server's details:

```sh
rsync -rv * your_username@your_server:set/
```

For development deployment, use the `dev.sh` script similarly.

## Development Tools and Requirements

For development, you will need:

- A CoffeeScript compiler for compiling `.coffee` files.
- A web server to serve the static files.
- `rsync` for deploying your changes.

## Credits and License

This game was originally created by [Steven Hao](http://stevenhao.com) and is currently maintained by the open-source community. The game and its source code are released under the MIT License.

Feel free to contribute to the repository, report issues, or fork it to create your own version.



