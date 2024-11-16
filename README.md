# Liquibase Helper: Java Shebang Script
A simple CLI utility for generating Liquibase UTC timestamps and change file templates. Written in pure Java using shebang script functionality.

## Prerequisites
- Java 21 or higher
- Unix-like environment (Linux, macOS, WSL)

## Installation
1. Download the script:
```bash
curl -O https://raw.githubusercontent.com/yourusername/liquibase-template-generator/main/liquibase-helper
```

2. Make it executable:
```bash
chmod +x ./liquibase-helper
```

3. Optional: Make it available system-wide:
```bash
sudo mv ./liquibase-helper /usr/local/bin/
```

## Usage
Run the script:
```bash
./liquibase-helper
```

Available commands:
- `timestamp`: Generate UTC timestamps for filename and changeset ID
- `generate`: Create a complete Liquibase change file template
- `help`: Show available commands
- `exit`: Exit the program

### Example Usage:
```bash
$ ./liquibase-helper
Liquibase Timestamp Helper - Type 'help' for commands or 'exit' to quit
Command> timestamp
Filename timestamp: 20241115T175648
Changeset ID timestamp: 20241115175648

Command> generate
Enter change description: create user table
Enter author name: anik.dev
Generated filename: 20241115T175708_create_user_table.xml
Generated changeset ID: 20241115175708
XML Content:
<?xml version="1.0" encoding="UTF-8"?>
<databaseChangeLog
    xmlns="http://www.liquibase.org/xml/ns/dbchangelog"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation="http://www.liquibase.org/xml/ns/dbchangelog
    https://www.liquibase.org/xml/ns/dbchangelog/dbchangelog-4.1.xsd">
    <changeSet id="20241115175708" author="anik.dev">
        <!-- Your changes here -->
    </changeSet>
</databaseChangeLog>
```

## Features
- Generates UTC timestamps in two formats:
  - Filename format: `yyyyMMdd'T'HHmmss`
  - Changeset ID format: `yyyyMMddHHmmss`
- Creates complete Liquibase XML templates
- Interactive CLI interface
- No external dependencies
- Direct execution through shebang

## How It Works
This script uses Java's shebang functionality (available since Java 11) to run directly from the shell. The shebang line:
```java
#!/usr/bin/java --source 21
```
tells the shell to execute the file using Java in source mode.

The implementation uses Java's modern features including:
- Records for template data structures
- Text blocks for multiline strings
- Pattern matching for switch expressions
- Modern date-time API with UTC handling

## Contributing
Feel free to open issues or submit pull requests. Any contributions are welcome!

## License
MIT License - see [LICENSE.md](LICENSE.md)

## Author
@Anik-Infinity : anik.kafi404@gmail.com
