# First steps in Swift

The simple hello worlds is the same as in python

``` swift
print("Hello World!")
```

But moving to variables and constants you observe the first differences - you need to declare them and their type first!

``` swift
let answerToLifeTheUniverseAndEverything = 42
```

Constants are declared with `let` and variables with `var`.

There is so much left to learn ... But I got something working on the first day that I program in other languages since 1992:

## Prime numbers

Here is the code:

``` swift
let lastNumber = 1000

print("We calcuate the prime numbers until", terminator: " ")
print(lastNumber)

print("2 3 5 7 11", terminator:" ")

for number in 13 ... lastNumber {
    let upperBound = Int(Double(number).squareRoot())
    var isPrime = 1
    for divisor in 2 ... upperBound {
        let quotient = Double(Double(number) / Double(divisor))
        let rest = quotient - Double(Int(quotient))
        //print(number, divisor, rest)
        if rest == 0 {
            isPrime = 0
            break
        }
    }
    if isPrime == 1 {
        print(number, terminator:" ")
    }
}
```

Now just have to measure the time to compare.
