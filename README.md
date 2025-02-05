# Unexpected Behavior when Directly Manipulating Ruby Instance Variables

This example demonstrates a potential issue when directly manipulating instance variables in Ruby using `instance_variable_set` and `instance_variable_get`. While these methods offer flexibility, they can bypass internal checks and validations within a class, potentially leading to unexpected behavior or inconsistencies.

The `bug.rb` file shows a scenario where modifying the instance variable `@value` directly using `instance_variable_set` circumvents any internal logic that may be associated with updating the value, possibly violating invariants or assumptions within the class.

The solution presented in `bugSolution.rb` suggests using a setter method, enforcing encapsulation, and allowing for controlled modification and validation of the instance variable.