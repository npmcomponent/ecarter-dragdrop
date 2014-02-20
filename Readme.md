*This repository is a mirror of the [component](http://component.io) module [ecarter/dragdrop](http://github.com/ecarter/dragdrop). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/ecarter-dragdrop`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# dragdrop

  simple drag and drop component

## Installation

    $ component install ecarter/dragdrop

## Features

* dead simple drag and drop event handling
* auto-binds to all `draggable="true"` children elements
* adds `dragging` and `over` classes for element styling
* no jquery dependency :+1:

## Events

* `start` (el) on drag start
* `enter` (el) when drag enters `draggable` target
* `over` (el) when drag is over target
* `leave` (el) when drag leaves target
* `end` (el) when drag event ends
* `drop` (drag, drop) when drag to drop completes

## Examples

Drag a element and replace it with another:

      var draggable = Dragdrop(el);

      draggable.on('drop', function(drag, drop){
        var dragged = drag.cloneNode(true);
        var dropped = drop.cloneNode(true);
        list.replaceChild(dragged, drop);
        list.replaceChild(dropped, drag);

        console.log('dropped element', drag, 'to element', drop);
      });

## License

  MIT
