

# SQL Insert Mapper

**SQL Insert Mapper** is a lightweight Java Swing application for formatting, parsing, and manipulating SQL `INSERT` statements. It provides a user-friendly GUI to extract columns and values, display them in a table format, and generate clean, well-formatted SQL queries.

---

## Features

* **Input Formatting**: Automatically parses and formats `INSERT INTO` SQL queries.
* **Column-Value Table**: Displays a clean, aligned table of columns and values for easy review.
* **Editable Table**: Users can directly edit values in the output table. Changes are reflected when generating or copying the SQL query.
* **Search & Highlight**: Search for specific values in the output table and navigate through matches.
* **Copy Clean SQL**: Generate a properly formatted `INSERT` query from the table and copy it to the clipboard.
* **Font Customization**: Adjust font size of input and output areas for readability.
* **Dark Theme UI**: Easy-on-the-eyes dark mode with customized scroll bars and styled buttons.

---

## Requirements

* Java **JDK 8 or above**
* Operating System: **Windows, macOS, Linux**

---

## Installation

1. Download the `InsertQueryFormatter.jar` file.
2. Ensure you have Java installed and added to your system PATH.
3. Launch the application:

   **Option 1: Double-click JAR**

   * Simply double-click the JAR file to open the GUI.

   **Option 2: Terminal/Command Prompt**

   ```bash
   java -jar InsertQueryFormatter.jar
   ```

---

## User Manual

### Main Interface

The application consists of three main areas:

1. **Top Bar**:

   * **Format Button**: Parse and format the input SQL query.
   * **Clear Input Button**: Clears the input text area.
   * **Copy Query Button**: Generates a clean SQL query from the column-value table and copies it to the clipboard.
   * **Font Size Dropdown**: Adjust the font size of both input and output areas.
   * **Search Field & Buttons**: Enter a search term, then click **Search**, **Next**, or **Prev** to navigate through matches in the output.

2. **Input Area**:

   * Paste or type your `INSERT INTO` SQL query here.
   * Example:

     ```sql
     INSERT INTO employees (id, name, salary) VALUES (1, 'John Doe', 50000);
     ```

3. **Output Area (Formatted Col-Value Table)**:

   * Displays a table of columns and corresponding values.
   * Users **can edit values directly** in the table.
   * This is especially useful when:

     * Mapping hundreds of columns and values.
     * Comparing existing data with new values.
     * Adding or removing columns or values.
   * Any changes made here are automatically included when clicking **Copy Query**.

---

### How to Use

1. **Enter SQL Query**: Paste your `INSERT INTO` statement in the input area.
2. **Format Query**: Click **Format** to parse the input and display a column-value table in the output area.
3. **Edit Table (Optional)**:

   * Modify values directly in the output area.
   * You can also remove or add lines manually if needed.
4. **Search Values**:

   * Enter a keyword in the search box.
   * Click **Search** to highlight all occurrences.
   * Use **Next** and **Prev** to navigate matches.
5. **Copy Clean SQL**:

   * After reviewing and editing the table, click **Copy Query** to generate a formatted SQL query with all modifications included.
   * The query is copied to the clipboard and ready for use.

---

### Example

**Input:**

```sql
INSERT INTO employees (id, name, salary) VALUES (1, 'John Doe', 50000);
```

**Output (editable table):**

```
COLUMN                                   | VALUE
-----------------------------------------------------------------------------------
id                                       | 1
name                                     | 'John Doe'
salary                                   | 50000
```

**Edited Output:**

```
COLUMN                                   | VALUE
-----------------------------------------------------------------------------------
id                                       | 101
name                                     | 'Jane Doe'
salary                                   | 60000
```

**Generated SQL:**

```sql
INSERT INTO employees (
    id,
    name,
    salary
) VALUES (
    101,
    'Jane Doe',
    60000
);
```

---

### Notes

* Queries must start with `INSERT INTO`.
* The number of columns and values must match; otherwise, an error will be displayed.
* Supports simple and nested values (like JSON objects or arrays) inside `VALUES`.
* The application automatically highlights searched text in the output table.
* Editable output table allows bulk mapping, comparison, or modifications before generating SQL.

---

### Customization & Theme

* **Dark Theme**: All panels, buttons, and text areas follow a dark color scheme.
* **Scroll Bars**: Thin, colored scrollbars match the theme.
* **Styled Buttons**: Hover effects for easy navigation.
* **Font Sizes**: Adjustable via dropdown menu.

---

### Known Limitations

* Only supports `INSERT INTO` SQL statements.
* Multi-line or unconventional SQL formatting may require cleanup before parsing.
* Nested parentheses in values are partially supported.

---

### License

This project is **open-source**. You may use and modify it freely. Attribution is appreciated.

