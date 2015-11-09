# snap.svg.rotate

Adds a `rotate` method to `Snap.Element`. It should on any element, scaled or
transformed in any way. If it does not: please report an issue.

## Usage

A `rotate` function is added to the `Snap.Element` prototype, which can be used
simply like this:

    // 90 degrees clockwise
    element.rotate(90);

    // 90 degrees counter-clockwise
    element.rotate(-90);

An event is emitted after rotating the element, which can be used like this:

    // Catch-all for rotation events. If you want to only listen to the event
    // for one element, replace the * with the id of the element. this in the
    // of the callback is the rotated element.
    eve.on('snap.rotated.*', function() {
        console.log(this, 'was rotated');
    });

    element.rotate(20);

## Installing

Our preferred method of installing this is through `npm`:

    npm install snap.svg.rotate

Although you can also install this by using `bower`:

    bower install snap.svg.rotate

Or just download the source file and include it *after* Snap.svg.

## License

This plugin is licensed under the Mozilla Public License v2.0.
