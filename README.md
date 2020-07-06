# Animation Task Manager, for Firefox older than its version 57.

This project is obsolete and not maintained anymore.

Usage:

    window['piro.sakura.ne.jp'].animationManager.addTask(
      function(aTime, aBeginningValue, aTotalChange, aDuration) {
        // some animation task runned by interval
        var current = someEasingFunction(aTime, aBeginningValue, aTotalChange, aDuration);
        target.style.left = current+'px';
        return aTime > aDuration; // return true if the animation finished.
      },
      100, // beginning
      200, // total change (so, the final value will be 100+200=300)
      250, // msec, duration
      window // the window (used by Firefox 4 animation frame API)
    );
    // stop all
    window['piro.sakura.ne.jp'].animationManager.stop();
    // restart after doing something
    window['piro.sakura.ne.jp'].animationManager.start();

