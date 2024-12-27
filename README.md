# Recursive Text Search and Replace

This Python script allows users to search for a specific text string within files located in the current directory and all its subdirectories. Optionally, the user can replace the text with another string.

## Features
- **Recursive Search:** Searches for a given text in all files within the current directory and its subdirectories.
- **Replacement Option:** Allows replacing the found text with another string.
- **Detailed Output:** Lists all occurrences of the search term along with file names and line numbers.
- **Error Handling:** Skips files that cannot be processed due to encoding issues or permission restrictions.
- **Large-Scale Replacements:** Efficiently handles large replacements, even for scenarios exceeding 20,000 occurrences, which may surpass the maximum limit in some editors like VS Code.

## Usage
This script requires Python 3.x. The script accepts command-line arguments for input. To use the script, navigate to the directory containing the script and run it as follows:

```bash
python main.py <search_text> [replace_text]
```

### Arguments
- `<search_text>` (required): The text string to search for in the files.
- `[replace_text]` (optional): The text string to replace the search term with.

### Examples
#### Search Only
To search for the word "example":
```bash
python main.py example
```

#### Search and Replace
To search for "example" and replace it with "sample":
```bash
python main.py example sample
```

## Output
- Lists each file where the search term is found.
- Displays the line number and the content of each matching line.
- Shows the total number of occurrences across all files.

### Example Output
```plaintext
Occurrences in ./file1.txt:
  Line 3: This is an example line.
  Line 7: Another example here.

Occurrences in ./subdir/file2.txt:
  Line 5: Example in a subdirectory.

Total occurrences of 'example': 3
```

If replacement is performed, the script updates the relevant files in place.

## Error Handling
- Skips files with unsupported encoding.
- Ignores files that the user does not have permission to read or write.

## Notes
- The script processes text files and may not handle binary or non-text file types appropriately.
- Ensure you have a backup of your files before running with the replace option, as changes are made in place.
- Especially useful for large-scale replacements involving thousands of occurrences, overcoming limitations of editors like VS Code.

## License
This script is provided under the [MIT License](https://opensource.org/licenses/MIT).

## Author
Yusuf Arslan [GitHub](https://github.com/yusufarsln98)

