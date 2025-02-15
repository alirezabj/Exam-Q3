# Exam-Q3


### A)

A record class is the best choice for storing customer database query results because it is immutable which means that its values cannot be changed after creation. This makes the data more reliable and prevents accidental modifications. Additionaly, records are also simple and efficient since they automatically generate constructors, getters, and methods which reduces unnecessary code. Moreoover, since each database entry follows a fixed structure (Name, Address, Email, Purchased Product, and Purchase Date), a record can store this information in a structured way. Other classes such as anonymous classes are typically used for temporary implementations, and enums are only useful when dealing with a fixed set of predefined values and therefore they are not suitable. Sealed classes are designed to limit inheritance which also do not fit this use case. Therefore, a record class is the best solution for this task.  


### B)

The best choice is function literals and interfaces. The reason is that the filter method signature `boolean filter(Entry entry)` describes a function. A functional interface allows defining this behavior in a reusable way and provides a concise implementation. This approach avoids rewriting loops and makes the filtering logic modular. Other options, such as static classes are used for organizing related classes which is unnecessary for a simple function or nested inner classes require an instance of the outer class, which is not needed for a reusable function. Moreover, literal classes are only useful for a fixed set of values, while our filter criteria are dynamic or records store immutable data but do not define behavior like filtering or sealed classes are used to restrict inheritance, which is irrelevant for a filtering function.



### C)

A sealed class is the best choice for modeling financial transactions because it allows defining a fixed set of transaction types (Deposit, Withdrawal, Transfer) while ensuring they all share a common structure. Transactions need value semantics which means that they represent specific amounts and types but behave differently from simple numbers like doubles. With a sealed class, we can clearly define each transaction type which makes it easy to display them ("Deposit of $100", "Withdrawal of €50") and perform operations on them. Other options such as records are not suitable because transactions involve behavior and different types, not just immutable data even though they have value semantics. Enum classes are not suitable because transactions require additional data (like amounts and currencies), and enums are too limited and inner or anonymous classes would make the design more complex. Moreover, function literals and interfaces are useful for defining behavior but not for structuring multiple transaction types.




























