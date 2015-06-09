# Cheats for Cookie Clicker

### Set Cookie Ammount
Game.cookies = Game.cookiesEarned + ammount;

### Spawn a Golden cookie Time for anytime peroid of your choice
Game.goldenCookie.time = 0;
Game.goldenCookie.spawn();

### Give yourself the final achivement
Game.Win('Cheated cookies taste awful');

### Remove the final achivement
Game.AchievementsById[70].won = 0;

### If you want 999,999,999,999,999,999 cookies use this
Game.RuinTheFun();

This will also gove you all of the upgrades.

### If you want to Change the CPS use this
Game.cookiesPs = CpS;

## Faster AutoClick
var autoClicker = function(clicksAtOnce, repeatInterval) {
    var cheated = false;
    var intoTheAbyss = function() {
        if(!cheated) {
            cheated = true;
            for(var i = 0; i < clicksAtOnce; i++) {
                Game.ClickCookie();
                Game.lastClick = 0;
            }
            cheated = false;
        };
    };
    return setInterval(intoTheAbyss, repeatInterval);
};
autoClicker(<amount of clicks>, <milliseconds interval>);
