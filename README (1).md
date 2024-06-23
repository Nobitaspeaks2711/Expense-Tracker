
# Expense Tracker

## Description

The Expense Tracker is a simple web application designed to help you keep track of your expenses. It allows users to input details about their expenses, categorize them, and view a summary in a table format.

## Features

- Add new expenses with a description, category, and amount.
- View a summary of all added expenses in a table.

## Technologies Used

- HTML
- CSS
- JavaScript

## Setup

1. **Clone the repository**

   ```bash
   git clone https://github.com/Nobitaspeaks2711/expense-tracker.git
   ```

2. **Navigate to the project directory**

   ```bash
   cd expense-tracker
   ```

3. **Open the `index.html` file in your web browser**

   ```bash
   open index.html
   ```

## Usage

1. Open the `index.html` file in your preferred web browser.
2. Fill out the expense description, select a category, and enter the amount.
3. Click on "Add Expense" to add the expense to the summary table.
4. The added expenses will be displayed in the "Expense Summary" table.

## Code Explanation

### HTML Structure

- The HTML structure includes a form for entering expense details and a table for displaying the expense summary.
- The form has three input fields: description, category (dropdown), and amount.
- The table has three columns: description, category, and amount.

### CSS Styling

- Basic styling is applied to the form and table for a clean and user-friendly interface.
- The `.container` class centers the content and applies padding and background styling.
- Input fields and buttons have consistent padding, border, and background colors.

### JavaScript Functionality

- The JavaScript code handles the form submission event.
- When the form is submitted, it prevents the default behavior and validates the input fields.
- If the inputs are valid, a new row is created in the table with the expense details.
- After adding the expense, the input fields are cleared for new entries.

### JavaScript Code

```javascript
const expenseForm = document.getElementById("expenseForm");
const expenseList = document.getElementById("expenseList()");

expenseForm.addEventListener('submit', function (event) {
    event.preventDefault();
    const description = document.getElementById('description').value;
    const category = document.getElementById('category').value;
    const amount = document.getElementById('amount').value;

    if (description && category && !isNaN(amount)) {
        const newRow = document.createElement('tr');

        newRow.innerHTML = `
            <td>${description}</td>
            <td>${category}</td>
            <td>${amount}</td>
        `;

        expenseList.appendChild(newRow);

        document.getElementById('description').value = '';
        document.getElementById('category').value = '';
        document.getElementById('amount').value = '';
    } else {
        alert('Please, fill out all fields with valid data.');
    }
});
```

## Contributing

If you would like to contribute to this project, please fork the repository and create a pull request with your changes.

## License

This project is licensed under the MIT License.

---



