## Broadcasting colours

In this step you will use `broadcasts`{:class="block3events"} so that when a colour is detected it has an affect on another sprite.

--- task ---

Import a new animal sprite into your project. You can choose any sprite you like, but in this example a **Toucan** will be used.

--- /task ---

--- task ---

Click on the **Costumes** tab and change the colour of the animal so that it matches one of the colours of your paper.

![image of the toucan sprite](images/animal-sprite.png)

--- /task ---

--- task ---

Now go back to your **target** sprite. In the `Events`{:class="block3events"} menu you can drag a `broadcast [message1 v] `{:class="block3events"} block and then create a new message

![image of the menu selection for a broadcast block](new-message.png)

Call the message `red` or whatever the first colour of your paper was.

![image showing the naming dialogue box, with red typed in](images/message-red.png)

--- /task ---

--- task ---

Add the new `broadcast`{:class="block3events"} block into your script, so it occurs when the camera sees the colour red.

![image of target sprite](images/target-sprite.png)

```blocks3
when flag clicked
set video transparency to [0]
turn video [on v]
set [ghost v] effect to [80]
forever
if <<touching color [#FF6E66] ?> or <touching color [#FF7E80] ?>> then
+ broadcast [red v]
say [red] for [2] secs
end
if <<touching color [#00D6FF] ?> or <touching color [#00D6FF] ?>>  then
say [blue] for [2] secs
end
if <<touching color [#62E09A] ?> or <touching color [#69E6A1] ?>> then
say [green] for [2] secs
end
``` 

--- /task ---

--- task ---

Repeat this for the other colours.

![image of target sprite](images/target-sprite.png)

```blocks3
when flag clicked
set video transparency to [0]
turn video [on v]
set [ghost v] effect to [80]
forever
if <<touching color [#FF6E66] ?> or <touching color [#FF7E80] ?>> then
broadcast [red v]
say [red] for [2] secs
end
if <<touching color [#00D6FF] ?> or <touching color [#00D6FF] ?>>  then
+ broadcast [blue v]
say [blue] for [2] secs
end
if <<touching color [#62E09A] ?> or <touching color [#69E6A1] ?>> then
+ broadcast [green v]
say [green] for [2] secs
end
```
--- /task ---

--- task ---

Click back to you animal sprite. Position and size your animal so if fits nicely on the left hand side of the **Stage**.

![image showing animal sprite on upper left hand side of the stage](sprite-on-stage.png)

--- /task ---




