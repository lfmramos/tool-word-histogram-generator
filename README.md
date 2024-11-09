# Word Histogram Generator

A Java implementation demonstrating two different approaches to creating a word histogram: inheritance and composition. This project analyzes text strings and generates frequency counts of words, showcasing Object-Oriented Programming principles and different design patterns.

## Features

- Count word frequencies in a given text string
- Two implementation approaches:
  - Composition-based (`WordHistogramComp`)
  - Inheritance-based (`WordHistogramInheritance`)
- Iterable interface implementation for easy word traversal
- Memory-efficient storage using HashMap

## Implementation Details

### Composition vs Inheritance

The project implements the same functionality using two different approaches to demonstrate their pros and cons:

#### Composition (`WordHistogramComp`)
- Uses a `HashMap` as an internal data structure
- Implements `Iterable<String>`
- Provides controlled access to the underlying map
- Better encapsulation and flexibility
- Follows "favor composition over inheritance" principle

#### Inheritance (`WordHistogramInheritance`)
- Extends `HashMap<String, Integer>`
- Implements `Iterable<String>`
- Direct access to all HashMap methods
- More concise implementation but less flexible

## Usage

### Basic Usage

```java
// Using Composition
WordHistogramComp histogramComp = new WordHistogramComp("your text here");
System.out.println("Distinct words: " + histogramComp.size());

// Using Inheritance
WordHistogramInheritance histogramInher = new WordHistogramInheritance("your text here");
System.out.println("Distinct words: " + histogramInher.size());

// Iterate through words and their frequencies
for (String word : histogramComp) {
    System.out.println(word + " : " + histogramComp.get(word));
}
```

### Example Output
For the input string "test word words test 1 10 1":
```
MAP has 6 distinct words
test : 2
word : 1
words : 1
1 : 2
10 : 1
```

## Technical Details

### Key Methods

Both implementations provide:
- `size()`: Returns the number of distinct words
- `get(String word)`: Returns the frequency of a specific word
- `iterator()`: Allows iteration over all words

### Data Structure

- Uses `HashMap` for O(1) access time
- Space complexity: O(n) where n is the number of unique words
- Time complexity: 
  - Word counting: O(n)
  - Word frequency lookup: O(1)

## Design Considerations

### Composition Advantages
1. Better encapsulation
2. More flexible for future modifications
3. Controlled interface exposure
4. Easier to maintain

### Inheritance Advantages
1. Less code duplication
2. Direct access to HashMap methods
3. Simpler implementation

## Getting Started

### Prerequisites
- Java Development Kit (JDK) 8 or higher
- Java IDE (recommended: IntelliJ IDEA or Eclipse)

### Running the Project

1. Compile the Java files:
```bash
javac io/codeforall/fanstatics/*.java
```

2. Run the main class:
```bash
java io.codeforall.fanstatics.Main
```

## Future Enhancements

Potential improvements could include:
1. Case-insensitive word counting
2. Punctuation handling
3. Support for file input
4. Statistical analysis features
5. Performance optimizations for large texts

## Contributing

Feel free to submit issues and enhancement requests!
