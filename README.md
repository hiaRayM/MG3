# MG3
## Devlog
Write your Devlog here.


1. After I tested, I found that the default value of float is 0.0, int is 0, bool is false, and string is null(which display a blank text field);

2. From my personal point of view, as long as the code is connect to unity and the method is directly named as "Update", the unity will automatically every frame on its own.

3. For KickWeapon use Timer to turn the kick hitbox off after a brief moment:

Firstly, when player presses the space,  the ActivateKick() will be called. then calls _lifeTimer.BeginTimer(_lifetimeSeconds) to start the countdown.

Secondly, inside KickWeapon's own Update() method, it checks every frame whether _lifeTimer.IsFinished() is true.

Thirdly, thus, when the timer reaches zero, it calls `gameObject.SetActive(false)` to disable the kick weapon.

For the timer itself, it will use the Time.deltaTime to count down every frame by using its own Update method to check the time status. This in order to last kick in a seconds but not for a long time.



## Open-Source assets
- [Cat fighter spritesheet](https://opengameart.org/content/cat-fighter-sprite-sheet)
- [Food sprites](https://rcpstd.itch.io/pixel-food-pack)
