# HW1 notes

Answer each question in a few sentences. Be specific: name the function, the error or the command.

## What did you try?
I did everything mostly to the spec provided in the readme. Used list comprehensions, setters and getters, inheritance with super(), and copy for mutable data. 

## What broke, and how did you fix it?
In PromoItem, i called self.cost() resulting in hitting max recursion depth. I fixed it by changing it to super().cost(). In the total function of the Order, I checked if food_cost >= self.free_delivery_from for when to NOT set the fee to 0, which is the opposite of intended behavior. I fixed it by flipping the condition. In summary func. of Order, I used "\n".join([f"{q} x {f.name}" for f, q in self.lines]) since I thought it needed a string with multiple lines of orders instead of a list. I fixed it by removing the join.

## What would you do differently next time?
I guess I'll test all the functions as I write them. Right now, I just write everything first, then test them all and debug them all. In an actual production environment I won't be that lazy.