# unreal_engine5

// section 2

- lecture 14
objects = collections of data and functionality
actors = object that can go in a level
component = objects that can go on an actor

ex) car (actor) 
        <- wheel (component)
        <- light (component)
        <- gas pedal (component) : if player 'hits the gas (component)', move a car. 

reference = where to find an object

cube's address -- find --> cube(what does static mesh component is?) -- find --> static mesh component(what's your name?) -- find --> "name"


- lecture 15

What I want to do is for this to actually apply a force upwards.
Now in actual fact, we don't want it to apply a force, but we want to have it apply something called an impulse.
Now, the difference between the two, in physics parlance, is that a force happens over a certain amount of time, whereas an impulse is instantaneous.

* force = mass * acceleration
* impulse(충격량) = mass * velocity change(속력)

So if we want a certain acceleration, we need to multiply it by the mass and that gives us the force required. There's also a similar equation for an impulse where actually if what you want is a change in velocity rather than an acceleration, then you essentially multiply that by the mass.

* add impulse : vel change (change acc to vel)


- lecture 16 : blueprint classes and instances

class : template or a blueprint in the regular sense of that word for objects.

ex) the adventurer (class) : default data(level = 1, hp = 50) + some functionality(jump, attack..). 원본
    -> advecturer 1 (instance) : he has his "own copy of that data" from the Adventurer class. 사본
    -> advecturer 2 (instance) : a second instance of the same class and they share the functionality. 사본
* benefit of this is twofold.
- 1) we're sharing all that functionality between these different objects.
- 2) any of that data that we haven't changed such is default data(level = 1, hp = 50), 
     if i changed level 1 to 2, it would changed it across all of the instances of the class as well.

BP_Projectile - these are linked copies. Making a change to a property in the BP projectile editor should change it for all instances.
                they are linked back to this blueprint class and they are instances of it.


- lecture 17 : 