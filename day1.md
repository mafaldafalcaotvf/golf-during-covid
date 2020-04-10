# Challenge 1 (10/4/2020)

Implement a function that given a list of 
natural numbers, returns the lowest number 
not present in the list.

## Premises

```
0 <= list size <= 2^16
len(unique(list)) = len(list)
```

## Examples

```
minFree of 1, 2, 3, 4, 5 returns 6
minFree of an empty list returns 1
minFree of 10, 5, 9, 2, 24, 3, 1 returns 4
```

## Solutions

### (Chars) Language by Name  

```haskell
cenas = cenas
```

### (24) Haskell by Mafalda   

```haskell
minFree x=head([1..]\\x)
```

### (72) Python by Mafalda   

```python
def minFree(l):return 1 if not l else min(set(range(1,max(l)+2))-set(l))
```

### (63) Rust by André Silva
```rust
let minFree=|x:Vec<u64>|(1..).filter(|i|!x.contains(i)).next();
```

### (54) Rust untyped by André Silva
```rust
let minFree=|x|(1..).filter(|i|!x.contains(i)).next();
```

### (47) Scala by André Silva
```scala
def minFree(x:Seq[Int])=(1 to 2<<15).diff(x)(0)
```

### (38) Scala untyped by André Silva
```scala
def minFree(x)=(1 to 2<<15).diff(x)(0)
```

### (33) Scalaskell by André Silva
```scala
minFree x=(1 to 2<<15).diff(x)(0)
```

### (51) JavaScript by André Silva
```javascript
minFree=x=>{for(i=1;;i++)if(!x.indexOf(i))return i}
```