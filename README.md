# Dynamic polymorphism with std::variant and concept

Dynamic polymorphism with `std::variant` and `cpp20 concept`. 

This i've seen the famous [talk](https://www.youtube.com/watch?v=bIhUE5uUFOA) of Sean Parent, inheritance is the base class of evil, i've looked for a better way to do dynamic polymorphism. Base on this [talk](https://www.youtube.com/watch?v=gKbORJtnVu8) of Mateusz Pusz, i implemented an alternative to inheritance using `std::variant` and adding constraint with `cpp20 concept`.

I present 2 versions. One where it's easy to add an opération but not to add a type and another where it's easy to add a type but not to add an operation. Both use `std::variant` and `cpp20 concept`.

`cpp20 concept` are use to add constraint to our code with zero cost abstraction. We do not pay the cost of the level of indirection due to the virtual table of inheritance, but we can still express and inforce our intent.
