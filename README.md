# Liquibase Helper: Java Shebang Script

A simple CLI utility for generating Liquibase UTC timestamps and change file templates. Written in pure Java using shebang script functionality.

## Prerequisites

- Java 21 or higher
- Unix-like environment (Linux, macOS, WSL)

## Installation

1. Download the script:
```bash
curl -O https://raw.githubusercontent.com/yourusername/liquibase-helper/main/liquibase-helper
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
Filename timestamp: 20241114153000
Changeset ID timestamp: 2024-11-14 15:30:00

Command> generate
Enter change description: add user table
Enter author name: john.doe

Generated filename: V20241114153000__add_user_table.xml
Generated changeset ID: 2024-11-14 15:30:00_add_user_table

XML Content:
<?xml version="1.0" encoding="UTF-8"?>
<databaseChangeLog...
```

## Features

- Generates UTC timestamps in two formats:
  - Filename format: `yyyyMMddHHmmss`
  - Changeset ID format: `yyyy-MM-dd HH:mm:ss`
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

## Contributing

Feel free to open issues or submit pull requests. Any contributions are welcome!

## License

MIT License - see [LICENSE.md](LICENSE.md)

## Author

Your Name (@Anik-Infinity)