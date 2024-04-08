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
## variales
### varaibles5.rs
- `shadowing`: using `let`

## primitive_types
### primitive_types3.rs
- shorthand to create an arry: `[elment; times]`
### primitive_types4.rs
- Ownership, borrow, ref: &
- slice: [ .. ]

## vector
### vecs1.rs
- macro: vec![elements... ]
### vecs2.rs
- two ways
    - direct: use `*` 
    - map: 
- used to do in the `*` way, now prefer the `map` way

## move_semantics
### move_semantics1.rs
- ownership, borrow: the new va. takes the ownership from the old, the old can not be accessible
- mutable
### move_semantics2.rs
- clone()
- mutally borrow a reference to its argument: the next exec
### 