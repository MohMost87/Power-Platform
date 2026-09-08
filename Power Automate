<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Introduction to Expressions in Power Automate</title>
    <style>
        :root {
            --primary-color: #0078d4;
            --bg-color: #f9f9f9;
            --text-color: #333333;
            --code-bg: #f3f2f1;
            --border-color: #e1dfdd;
        }
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            background-color: var(--bg-color);
            margin: 0;
            padding: 20px;
        }
        .container {
            max-width: 900px;
            margin: 0 auto;
            background: #ffffff;
            padding: 40px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        h1, h2, h3 {
            color: var(--primary-color);
        }
        h1 {
            border-bottom: 2px solid var(--border-color);
            padding-bottom: 10px;
        }
        code {
            background-color: var(--code-bg);
            padding: 2px 6px;
            border-radius: 4px;
            font-family: Consolas, Monaco, monospace;
            font-size: 0.95em;
        }
        pre {
            background-color: var(--code-bg);
            padding: 15px;
            border-radius: 6px;
            overflow-x: auto;
            border: 1px solid var(--border-color);
        }
        pre code {
            background-color: transparent;
            padding: 0;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        th, td {
            border: 1px solid var(--border-color);
            padding: 12px;
            text-align: left;
        }
        th {
            background-color: var(--code-bg);
        }
        .note {
            background-color: #eff6fc;
            border-left: 4px solid var(--primary-color);
            padding: 15px;
            margin: 20px 0;
            border-radius: 0 4px 4px 0;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Introduction to Expressions in Power Automate</h1>
    
    <p>When building flows in Microsoft Power Automate, standard dynamic content allows you to pass data from one step to the next. However, when you need to manipulate text, format dates, perform math, or filter data dynamically, you need to use <strong>Expressions</strong>.</p>

    <h2>What is an Expression?</h2>
    <p>An expression is a formula used in Power Automate to perform operations like data manipulation, logical evaluations, conversions, and mathematical calculations. Expressions are written using a rich library of built-in functions.</p>

    <div class="note">
        <strong>Tip:</strong> Unlike dynamic content (which appears with a lightning bolt icon in a grey box), expressions are written inside the expression editor and appear in a purple/pink box once saved.
    </div>

    <h2>Anatomy of an Expression</h2>
    <p>Expressions always consist of a <strong>function name</strong> followed by parentheses <code>()</code> containing parameters (arguments). Parameters can be dynamic content, static strings, numbers, or even other nested expressions.</p>
    
    <pre><code>functionName(parameter1, parameter2)</code></pre>

    <p><strong>Example:</strong> Combining a first name and last name into a single string using <code>concat()</code>.</p>
    <pre><code>concat(outputs('Get_user_profile')?['givenName'], ' ', outputs('Get_user_profile')?['surname'])</code></pre>

    <h2>Common Expression Functions</h2>
    <p>Power Automate supports dozens of functions categorized by their use case:</p>

    <table>
        <thead>
            <tr>
                <th>Category</th>
                <th>Function Name</th>
                <th>Description</th>
                <th>Example</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td><strong>String</strong></td>
                <td><code>concat()</code></td>
                <td>Combines two or more strings together.</td>
                <td><code>concat('Hello ', 'World')</code></td>
            </tr>
            <tr>
                <td><strong>String</strong></td>
                <td><code>toLower()</code> / <code>toUpper()</code></td>
                <td>Converts text to lowercase or uppercase.</td>
                <td><code>toUpper('test')</code> &rarr; <code>TEST</code></td>
            </tr>
            <tr>
                <td><strong>Date & Time</strong></td>
                <td><code>utcNow()</code></td>
                <td>Returns the current timestamp in UTC.</td>
                <td><code>utcNow()</code></td>
            </tr>
            <tr>
                <td><strong>Date & Time</strong></td>
                <td><code>formatDateTime()</code></td>
                <td>Formats a timestamp into a custom string pattern.</td>
                <td><code>formatDateTime(utcNow(), 'yyyy-MM-dd')</code></td>
            </tr>
            <tr>
                <td><strong>Logical</strong></td>
                <td><code>equals()</code></td>
                <td>Compares two values to see if they are equal.</td>
                <td><code>equals(variables('Status'), 'Active')</code></td>
            </tr>
            <tr>
                <td><strong>Math</strong></td>
                <td><code>add()</code></td>
                <td>Adds two numbers together.</td>
                <td><code>add(5, 10)</code> &rarr; <code>15</code></td>
            </tr>
        </tbody>
    </table>

    <h2>How to Add an Expression in Power Automate</h2>
    <ol>
        <li>Open your flow designer and click on an input field where you want to add data.</li>
        <li>Select the <strong>Dynamic content</strong> menu that pops up.</li>
        <li>Switch from the <em>Dynamic content</em> tab to the <strong>Expression</strong> tab.</li>
        <li>Type your formula or function into the editor box.</li>
        <li>Click <strong>Add</strong> to save the expression to your action parameter.</li>
    </ol>

    <h2>Best Practices</h2>
    <ul>
        <li><strong>Use Descriptive Variable Names:</strong> Keeping your dynamic content and variable names clear makes referencing them in expressions much easier.</li>
        <li><strong>Test incrementally:</strong> Use Compose actions to test complex nested expressions before embedding them into critical actions like sending emails or updating databases.</li>
        <li>Watch out for syntax errors like missing commas or unmatched parentheses.</li>
    </ul>

</div>

</body>
</html>
