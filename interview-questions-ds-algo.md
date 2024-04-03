STRING
    How to you print duplicate character from a string ?

     fun printDuplicateCharacters(str: String) {
         val charCount = HashMap<Char, Int>()

          // Count occurrences of each character in the string
         for (char in str) {
            charCount[char] = charCount.getOrDefault(char, 0) + 1
         }

          // Print duplicate characters
          for ((char, count) in charCount) {
            if (count > 1) {
                println("$char - $count times")
            }
          }
      }

    fun main() {
        val inputString = "hello world"
        printDuplicateCharacters(inputString)
    }
