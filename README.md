# karma-speckle-reporter

Simple Karma reporter module that allows for greater configuration options than other existing packages.

Based on `karma-spec-reporter-2` which is based on `karma-spec-reporter` which is based on mocha's spec reporter.

# Installation

```bash
  $ npm install karma-speckle-reporter
```

There are few configuration that you could apply to the reporter.
``` js
//karma.conf.js
...
  config.set({
    ...
      reporters: ["spec"],
      specReporter: {

        // When test(s) fail - report it at the end of all tests 
        lateReport:      true,

        // Max error log lines to display
        maxLogLines:     5,

        // Don't show failed tests
        suppressFaild:   false,

        // Don't show successful tests
        suppressSuccess: false,

        // Don't show skipped tests
        suppressSkipped: false,

        // Determine which tests will be shown as slow
        slowTestTime: 40,
        fastTestTime: 20

      },
      plugins: ["karma-speckle-reporter"],
    ...
```

Take a look at the [karma-spec-reporter-example](http://github.com/mlex/karma-spec-reporter-example) repository to see the original reporter in action.
