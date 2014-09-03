# The Zombie Apocalypse

What can game theory tell us about how to deal with the zombie apocalypse?  I'm not really sure but this is the beginnings of an evolutionary spatial game using agent based modeling that might give us a clue.

At the moment, this is just a fork of some previous game theory simulations I've done, with the addition of a zombie strategy and payoff matrix.  The work that needs to be done is:

- conditional strategy updates 
	- zombies should infect cooperating humans
	- zombies should be killed or cured



## Usage

Fork this repo and then just open `index.html` in any browser and the simulation will automatically run.


## Customisation

Customising the simulation is easy.  Code of note is organised thusly:

		/
		- assets
			- styles.css
			- browser.js
			- d3.min.js
		- simulation.coffee.md
		- browser.coffee.md
		- index.html

Simulation logic is found in `simulation.coffee.md` while presentation code and D3.js hacks are in `browser.coffee.md`.  To alter the simulation, edit thse files and don't go touch'n `browser.js`.

The coffeescript files need to be built and compiled into `browser.js`.  To build, type the following:

		browserify -t coffeeify browser.coffee.md > assets/browser.js

You'll need to install browserify and coffeeify if you haven't already.

Licensed under a CC-BY-SA license.