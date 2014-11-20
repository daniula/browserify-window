# browserify-window

Crazy small package which gives option to export module to global scope for debugging.

{{{
    require('browserify-window').obj = obj;
}}}

To hide exported objects in production build all we need to do is add `ignore` parameter:

{{{
    browserify: {
        prod: {
            options: {
                debug: false,
                ignore: ['browserify-window'],
            },
            src: 'src/js/app.js',
            dest: 'build/js/app.js',
        }
    }
}}}