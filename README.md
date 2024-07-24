# JavaScript Variables

JavaScript provides three ways to declare variables:

## var

- **Scope**: Function scope
- **Mutability**: Can be redeclared and reassigned

```javascript

var x = 5;
var x = 10; // Redeclaration is allowed
x = 6; // Reassignment is allowed


let
Scope: Block scope
Mutability: Can be reassigned but not redeclared in the same scope

let x = 4;
let x = 6; // Error: Declaration is not allowed in the same scope
x = 5; // Reassignment is allowed

const
Scope: Block scope
Mutability: Cannot be reassigned or redeclared

const x = 7;
x = 9; // Error: Reassignment is not allowed

