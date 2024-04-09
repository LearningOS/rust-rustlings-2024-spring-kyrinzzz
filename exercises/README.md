# Exercise to Book Chapter mapping

| Exercise               | Book Chapter        |
| ---------------------- | ------------------- |
| variables              | §3.1                |
| functions              | §3.3                |
| if                     | §3.5                |
| primitive_types        | §3.2, §4.3          |
| vecs                   | §8.1                |
| move_semantics         | §4.1-2              |
| structs                | §5.1, §5.3          |
| enums                  | §6, §18.3           |
| strings                | §8.2                |
| modules                | §7                  |
| hashmaps               | §8.3                |
| options                | §10.1               |
| error_handling         | §9                  |
| generics               | §10                 |
| traits                 | §10.2               |
| tests                  | §11.1               |
| lifetimes              | §10.3               |
| iterators              | §13.2-4             |
| threads                | §16.1-3             |
| smart_pointers         | §15, §16.3          |
| macros                 | §19.6               |
| clippy                 | §21.4               |
| conversions            | n/a                 |

>have done the orginal rustlings test before, try again and also get something to learn

# Potholes
## 0 variales
### varaibles5.rs
- `shadowing`: using `let`

## 1 primitive_types
### primitive_types3.rs
- shorthand to create an arry: `[elment; times]`
### primitive_types4.rs
- Ownership, borrow, ref: &
- slice: [ .. ]

## 2 vector
### vecs1.rs
- Vec::new()
- macro: vec![elements... ]
### vecs2.rs
- two ways
    - direct: use `*` 
    - map: 
- used to do in the `*` way, now prefer the `map` way

## 3 move_semantics
### move_semantics1.rs
- ownership, borrow: the new va. takes the ownership from the old, the old can not be accessible
- mutable
### move_semantics2.rs
- clone()
- mutally borrow a reference to its argument: the next exec
### move_semantics6.rs
- ownership

## 4 struct 
### structs3.rs
- `self`

## 5 enums
### enums3.rs
- `match`
    ``` Rust
    match expr1 {
        type1 => { expr2 },
        type2(var) => { expr3 },
        _ => {}
    }

    ```
- match allows us to compare a value to a series of patterns and execute the code based on the matching pattern
    - A pattern can consist of literal quantities, variables, wildcards, and many other things
    - bind partial values of matching patterns
- the return value of one branch is the return value of the whole match expection 

## 6 strings
### string1.rs
- lifetime
- to_string()
- From
### strings3.rs
- RTFD(RTFM): Read the fxxxx document(mannul)
- STFW
### string4.rs
- std

## 7 modules
### modules1.rs
- private default
- `pub`
### modules2.rs
- `use xx as xxx`
### modules3.rs
- `use xx :: {yy, zz}`

## 8 HashMap
### hashmap1.rs
- <key, value>
- Hash::new()
- insert()
### hashmap2.rs
- `entry()` and `or_insert()`
### hashmap3.rs
- well, read the answer I wrote last time
- have ideas, but stuck on &mut T 

## quiz2.rs
- stuck on modules and strings for a while

## 9 Options
### options1.rs
- Option<T>, Some(), None
- unwrap() or match
- read the answer of match way
### options2.rs
- `if let` statement and `while let` statement
- read the answer: think in the reverse way, .unwrap() -- Some()
### options3.rs
- >Bind by reference during pattern matching. 
  > ref annotates pattern bindings to make them borrow rather than move. 
  > It is not a part of the pattern as far as matching is concerned: it does not affect whether a value is matched, 
  > only how it is matched.

## 10 error_handling
### error1.rs
- Result<T, E>
  - Ok(T)
  - Err(E)
### error2.rs
- ? -- match
- >If the value of Result is OK, the expression will return the value in OK and the program will continue. 
If the value is Err, Err is used as the return value for the entire function, 
as if the return keyword were used, so that the error value is propagated to the caller.
### error3.rs
- the ? is valid only in function that -> Result<T, E>
- in main function, use `()` to present nothing needed
### error4.rs
- kind of read the answer
### error5.rs
- trait 
- Box\<T\>: A pointer type that uniquely owns a heap allocation of type T.
- dyn
### error6.rs
- stuck, read the answer; .map_err()

## 11 generics
### generics2.rs
- `<T>`
    - functions: fn func_name<T>(arg: T) -> T
    - structs: struct StructName<T>
    - traits: trait TraitName<T>
    - impl<T> StructName<T> { ... }

## 12 traits
### traits1.rs
- trait: A trait defines a set of behaviors that can be shared, and once the train is implemented, you can use that set of behaviors.
  - similar to interface
- trait trait_name { ... }
  - impl trait_name for StructName { ... }
### traits4.rs
- traits as parameters
### traits5.rs
- multiple traits: impl Trait1 + Trait2 + Trait3 for StructName { ... }

## quiz3.rs
- stuck, but according to the compiler info, fix it

## 13 lifetimes
### lifetimes1.rs
- lifetime: When returning a reference from a function,the lifetime parameter for the return type needs to match the lifetime parameter for one of the parameters
  - follow the compiler
  - 'a: fn funcName<'a>(x : 'a i32) -> &'a str
### lifetimes2.rs
- same mark, same lifetime
- paths:
  - make y live longer
  - make println! inner
### lifetimes3.rs
- lifetime in struct: struct StructName<\'a> { field: \'a type1 } 

## 14 tests
### tests1.rs
- assert!(condition, "{}", message)
### tests4.rs
- attribute `should_panic`

## 15 iterators
### iterators1.rs
- iter(), next ()
