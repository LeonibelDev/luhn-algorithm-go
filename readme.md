
# Luhn Algorithm Implementation in Go

This project implements the Luhn algorithm in Go, a simple checksum formula used to validate various identification numbers, especially credit card numbers. The Luhn algorithm helps ensure that the number follows a valid structure, reducing the likelihood of errors in identification numbers.

## Features

- **String to Integer Conversion**: A function to convert strings to integers.
- **String Reversal**: A function to reverse a string, as required by the Luhn algorithm.
- **Credit Card Validation**: A function to validate a credit card number based on the Luhn algorithm.

## How the Luhn Algorithm Works

The algorithm follows these steps:

1. Reverse the credit card number.
2. Double every second digit starting from the second digit.
3. If the doubled number is greater than 9, subtract 9 from it.
4. Sum all the digits (modified and unmodified).
5. If the total sum is divisible by 10, the card number is valid. Otherwise, it is invalid.

## Example Usage

You can test the credit card validation with the following example:

```go
package main

import "fmt"

func main() {
    cardNumber := 1234567812345670
    isValid := validateCC(cardNumber)
    fmt.Println("Is the card number valid?", isValid)
}
```

In this example, the `validateCC` function will return `true` or `false` depending on whether the card number is valid according to the Luhn algorithm.

## Functions

### `stringToInt(s string) int`
Converts a string to an integer. Returns the integer value, or prints an error if the conversion fails.

### `reverse(s string) string`
Reverses the input string and returns the reversed version.

### `validateCC(ccnumbers int) bool`
Validates a credit card number based on the Luhn algorithm. Takes an integer (the credit card number) as input and returns `true` if the number is valid and `false` otherwise.

## Requirements

- Go 1.18 or higher

## How to Run

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/yourusername/luhn-algorithm-go.git
   cd luhn-algorithm-go
   ```

2. Run the Go program:

   ```bash
   go run main.go
   ```

3. The program will output whether the card number is valid or not.

## References

- [Luhn Algorithm on Wikipedia](https://en.wikipedia.org/wiki/Luhn_algorithm)

## Developer

- **x.com**:  @SrLeonibel

## License

This project is licensed under the MIT License - see the [LICENSE](https://mit-license.org/) file for details.