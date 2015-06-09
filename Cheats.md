# Cheats for Cookie Clicker

### If you dont want the "Cheated cookies tase awful" achivement use this
/*Game.goldenCookie.wrath = 0;*/
Game.goldenCookie.time = Game.goldenCookie.minTime;
Game.goldenCookie.life = 0;
Game.goldenCookie.spawn();

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

### Free Buildings
Game.ObjectsById.forEach(function (e) {
    e.basePrice = 0;
    e.refresh();
});
Game.storeToRebuild = 1;

### Original building Price
Game.priceIncrease = 1;
Game.ObjectsById.forEach(function (e) {
     e.refresh();
});
Game.storeToRebuild = 1;

### little note
http://bfy.tw/FEM
