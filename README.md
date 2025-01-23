# Ruby Bug: Instance Variable Manipulation

This example demonstrates a common but subtle bug in Ruby related to the use of `instance_variable_set` to modify instance variables. While this method provides direct access, it is generally discouraged for several reasons:

* **Bypass of Encapsulation:** It directly bypasses the class's methods, potentially causing unexpected changes that are not tracked or handled properly.
* **Maintainability Issues:**  When instance variables are modified directly, it makes the code harder to understand, debug, and maintain.  Changes can be harder to track if not done through defined methods.
* **Testability Concerns:**  Direct manipulation can make it harder to unit test your code, as the internal state is modified without passing through controlled interfaces.

The solution involves utilizing accessor methods for managing instance variables which ensures better control and maintainability.