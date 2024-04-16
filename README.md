# WYAG (Write Your Awesome Git)

Wyag is a Python3-based Git implementation, designed to help you understand the inner workings of Git by writing your own Git-like tool.

## Features

- **Initialization**: Initialize a new Wyag repository.
- **Cat-file**: Display the type and content of objects in the repository.
- **Log**: Generate a DOT file for the commit history and convert it to PDF.
- **Rev-parse**: Parse revision (commit, tree) types from given references.
- **Check-ignore**: Check if files are ignored by the repository.
- **Status**: Show the status of the repository.
- **Ls-files**: List files in the index with verbose information.

## Installation and Usage

### Prerequisites

    Python 3

### Building

1. Clone the repository:

    ```bash
    git clone https://github.com/himanshunanda22/WYAG.git
    ```

2. Navigate to the project directory:

    ```bash
    cd wyag
    ```
3. Command you infer:-
- Initialization:  To initialize a new Wyag repository, run:

```bash
python3 wyag init test
```
- Cat-file: To display the type and content of objects in the repository, use:

```bash
python3 wyag cat-file TYPE OBJECT
```
- Log: To generate a DOT file for the commit history and convert it to PDF, execute:

```bash
git log #to get the list of commits and then replace that hash in the next line
python3 wyag log e03158242ecab460f31b0d6ae1642880577ccbe8 > log.dot
dot -O -Tpdf log.dot
```
- Rev-parse: To parse revision (commit, tree) types from given references, use:

```bash
python3 wyag rev-parse --wyag-type commit HEAD
python3 wyag rev-parse --wyag-type tree HEAD
```
- Check-ignore: To check if files are ignored by the repository, run:

```bash
python3 wyag check-ignore hello.el hello.elc hello.html wyag.zip wyag.tar
```
- Status: To show the status of the repository, execute:

```bash
python3 wyag status
```
- Ls-files: To list files in the index with verbose information, use:

```bash
python3 wyag ls-files --verbose
```
### License
This project is licensed under the MIT License - see the LICENSE file for details.

### References
https://wyag.thb.lt/
