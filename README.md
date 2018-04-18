# Duper

This is a simple elixir command line application that helps find all the duplicate files in a directory.

The main purpose of this app was just to have some fun and experiment with elixir, so it should not be used in a production environment.

It also needs some finishing touches and polishing to make it generally useful as a tool.

## Installation

This simple application is not available through hex.pm, and if you want to play with it the best way is just to fetch the Github repository.

## Usage

To use the tool all you have to do is define your target directory in the application.ex file.

```
    children = [
      Duper.Results,
      { Duper.PathFinder, "ADD PATH TO TARGET DIRECTORY" },
      Duper.WorkerSupervisor,
      { Duper.Gatherer, 1 }
    ]
```
Then to run the application, all you have to do is run this command on the command line while inside the application folder:

```
mix run
```
