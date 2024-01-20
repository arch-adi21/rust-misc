## What is overflow error ?
Overflow error refers to a situation were , you assign values to a variable higher than it can hold. For suppose there exists an _'i8' (signed integer)_ type integer where u can only store integers ranging from _-128 to 127_. If you assign a variavle with 'i8' type a value greater than 127 or smaller than -128 , it will throw an overflow error. 

> Partical Example :
```
fn main () {
    let a : i8 = 129
    println!("{}",a)
}
```
This code is very likely to throw an overflow error stated below.
```
error: literal out of range for `i8`
 --> main.rs:2:18
  |
2 |     let a : i8 = 129;
  |                  ^^^
  |
  = note: the literal `129` does not fit into the type `i8` whose range is `-128..=127`
  = help: consider using the type `u8` instead
  = note: `#[deny(overflowing_literals)]` on by default

error: aborting due to previous error
```

## Fix :)
Chill man , just change your datatype to a suitable type. Here is [<-- Link -->]([url](https://labviewwiki.org/wiki/Integer_data_type)) attached where you can find your suitable datatype.
