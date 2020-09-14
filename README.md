$ and # conversion in Pd

The original facebook query:

"hi,

I have identified three potential issues with my patch - the context of the full patch is explored in the video below but I have summarised the main issues here:

1. on creating an object (e.g. a toggle) with a label or encoded s/r message, if that label or message contains a # it will get re-converted to "$". then, on saving and reloading the file, the label will change to just "0". I believe there is a reason for that (#s interfere with Pd code since "#X" means new line of code). but I want to find a way, if it is possible, to keep the #s. I have tried a thing that works in some programming languages which is to type "/#/" to say "this character is not a part of the code" - if that's what the issue is. but so far that hasn't worked.

2. the above issue also works in reverse: $ arguments can get converted into # arguments when coded into an object (again, it's for toggles specifally). in the video, I explained why I need both "$0" and "$1" arguments converted into messages. (I also explained my concern that a "#2" message converted into a "$2" argument might have some functional coding issues I might not be aware of in the video @6m22s through to 7m50s). the weird thing about this is that the "$0-" at the beginning of a message remains in tact but the unhyphenated "$1" argument at the end of the message does not. (it only just occured to me that the hyphen could be the thing preventing that for $0 but I'm posting this in case it's not - I will go check afterwards).

3. the final issue is that I created some tables in an abstraction turned graph that contain $1 arguments in order to make it possible for me to create different graphs on creating multiple instances of an abstraction through dynamic patching (see in video: 0m10s to 0m45s. the problem is the main patch doesn't accept those arguments for some reason but spits back "$1 arguments out of range" error messages (you can see this more clearly in the video @10m25s through to 13m55s). 

full code: can be downloaded from AydinHumphries/-and-conversion-in-Pd (github.com)

video: https://youtu.be/0KUmxHc_mqg"
