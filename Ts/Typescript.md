# Important notes for TypeScript

## Key Guidelines for TypeScript types.
1. Use PascalCase for type alias names.
2. Keep names descriptive and meaningful.
3. Use aliases for complex or repetitive types like unions, intersections, and object structures.
4. Document the alias if it represents a non-obvious type.
5. Prefer interfaces for defining object types when inheritance is needed.
6. Avoid unnecessary or overly simplistic type aliases for things like type Name = string.

## Interfaces vs. Type Aliases
Although interfaces and type aliases can often be used interchangeably to describe the shape of an object, there are some differences:

| Feature                    | Interface                                          | Type Alias                                            |
|----------------------------|----------------------------------------------------|-------------------------------------------------------|
| Extending	                 | Can be extended using extends	                  |Can be extended using intersections (&)                |
| Declaration Merging	     | Multiple declarations with the same name can merge |Type aliases cannot merge                              |
| Object or Function Types   | Mainly used for object and function shapes	      |Can be used for any type (primitives, unions, etc.)    |
| Flexibility in Inheritance | Supports inheritance of properties and methods	  |Supports composition using union and intersection types| 

## Key Guidelines for Interfaces

1. Use PascalCase: Interface names should be capitalized.
2. Descriptive names: Use meaningful names for your interfaces to improve code readability.
3. Optional properties: Use ? for optional properties.
4. Read-only properties: Use readonly to prevent modifications to properties.
5. Extend interfaces: Use extends to inherit properties from other interfaces.
6. Use for object types: Interfaces are typically better for defining object shapes compared to type aliases.
7. Declaration merging: Interfaces can merge, making them flexible for library extensions.
8. Use with classes: Interfaces are commonly used with classes to enforce implementation contracts.

## Key Concepts for Classes

1. Class: Defines properties and methods.
2. Constructor: Initializes class properties.
3. Public, Private, and Protected: Controls access to class members.
4. Readonly: Prevents modification of properties.
5. Getters and Setters: Controls access to properties.
6. Inheritance: A class can extend another class to inherit properties and methods.
7. Abstract Classes: Cannot be instantiated directly, but can be extended.
8. Static Members: Belong to the class, not the instance.
9. Constructor Overloading: Allows multiple ways to create instances.
10. Interfaces with Classes: Ensures a class follows a specific structure.

## Why Use an Underscore?

1. Convention: Indicates that the property is for internal use and should not be accessed directly from outside the class.
2. Distinguish private from public: Differentiates private variables (e.g., _age) from public getters/setters (e.g., age).
3. Historical Reasons: Used in JavaScript before private existed.
4. Optional in TypeScript: It's not required because TypeScript enforces private access control, but some developers still follow this naming pattern for clarity.