# Variables

In Rust, variable bindings are <span style="background:#369;border-radius:5px; padding:3px 5px; color:white">immutable</span> by default. When a variable is immutable, after a value is bound to a name, you can't change that value.

To mutate a value, we must first use the <span style="background:#369;border-radius:5px; padding:3px 5px;color:white">mut</span> keyword to make a variable binding mutable.

```rust
// immutable variable by default rule of the Rust
let immutable_variable:i64 = 23;

// Declare the mutable variable with `mut` keyword
let mut mutable_vaiable:$str= "This is the mutable variable which declared with `mut` keyword".
```

# Define an Enum

```rust
enum WebEvent {
    // An enum variant can be like a unit struct without fields or data types
    WELoad,
    // An enum variant can be like a tuple struct with data types but no named fields
    WEKeys(String, char),
    // An enum variant can be like a classic struct with named fields and their data types
    WEClick { x: i64, y: i64 }
}
```

The enum in our example has three variants of different types:

- WELoad has no associated data type or data.
- WEKeys has two fields with data types String and char.
- WEMClick contains an anonymous struct with named fields x and y, and their data types (i64).

# Define an enum with structs

```rust
// Define a tuple struct
struct KeyPress(String, char);

// Define a classic struct
struct MouseClick { x: i64, y: i64 }

// Redefine the enum variants to use the data from the new structs
// Update the page Load variant to have the boolean type
enum WebEvent { WELoad(bool), WEClick(MouseClick), WEKeys(KeyPress) }
```

# Instantiate an enum

##### Simple variant: WELoad(bool)

```rust
let we_load = WebEvent::WELoad(true);
```

##### Struct variant: WEClick(MouseClick)

```rust
// Instantiate a MouseClick struct and bind the coordinate values
let click = MouseClick { x: 100, y: 250 };

// Set the WEClick variant to use the data in the click struct
let we_click = WebEvent::WEClick(click);
```

##### Tuple variant: WEKeys(KeyPress)

```rust
// Instantiate a KeyPress tuple and bind the key values
let keys = KeyPress(String::from("Ctrl+"), 'N');

// Set the WEKeys variant to use the data in the keys tuple
let we_key = WebEvent::WEKeys(keys);
```
