<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MedusaApp README</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            color: #333;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }
        h1, h2 {
            color: #2c3e50;
        }
        code {
            background-color: #f4f4f4;
            padding: 2px 4px;
            border-radius: 4px;
        }
        pre {
            background-color: #f4f4f4;
            padding: 10px;
            border-radius: 4px;
            overflow-x: auto;
        }
    </style>
</head>
<body>
    <h1>MedusaApp</h1>
    <p>MedusaApp is a full-stack e-commerce application built with Medusa, featuring both frontend and backend components.</p>

    <h2>Project Structure</h2>
    <ul>
        <li><code>backend/</code>: Contains the Medusa backend application</li>
        <li><code>storefront/</code>: Contains the Medusa storefront application (Next.js)</li>
        <li><code>docker-compose.yml</code>: Docker configuration for the project</li>
    </ul>

    <h2>Prerequisites</h2>
    <ul>
        <li>Node.js version 14 or later</li>
        <li>Docker and Docker Compose</li>
        <li>Yarn package manager</li>
    </ul>

    <h2>Getting Started</h2>
    <ol>
        <li>
            <p><strong>Start Docker:</strong><br>
            Ensure Docker is running on your machine before proceeding.</p>
        </li>
        <li>
            <p><strong>Install dependencies:</strong><br>
            Open a terminal and run the following commands:</p>
            <pre><code>

# Install backend dependencies

cd backend
yarn install

# Install storefront dependencies

cd ../storefront
yarn install
</code></pre>

</li>
<li>
<p><strong>Set up environment variables:</strong><br>
Create <code>.env</code> files in both <code>backend/</code> and <code>storefront/</code> directories with the necessary environment variables.</p>
</li>
<li>
<p><strong>Start the application:</strong><br>
From the root directory of the project, run:</p>
<pre><code>docker-compose up</code></pre>
<p>This will start the required services (PostgreSQL, Redis, etc.).</p>
</li>
<li>
<p><strong>Start the backend and storefront:</strong><br>
In separate terminal windows, run:</p>
<p>For the backend:</p>
<pre><code>cd backend
yarn dev</code></pre>
<p>For the storefront:</p>
<pre><code>cd storefront
yarn dev</code></pre>
</li>
</ol>
<p>Now your Medusa backend should be running on <code>http://localhost:9000</code> and the storefront on <code>http://localhost:3000</code>.</p>

    <h2>Features</h2>
    <ul>
        <li>Product management</li>
        <li>Order processing</li>
        <li>Customer accounts</li>
        <li>Shopping cart functionality</li>
        <li>Checkout process</li>
        <li>[Add any specific features of your implementation]</li>
    </ul>

    <h2>API Documentation</h2>
    <p>The Medusa backend provides a RESTful API. You can access the API documentation at <code>http://localhost:9000/store/docs</code> when your backend server is running.</p>

    <h2>Customization</h2>
    <h3>Backend</h3>
    <p>To add custom endpoints or services:</p>
    <ol>
        <li>Create new files in the <code>src/api</code> directory for API routes.</li>
        <li>Add services in the <code>src/services</code> directory.</li>
        <li>Use the <code>src/subscribers</code> directory for event subscribers.</li>
    </ol>

    <h3>Storefront</h3>
    <p>The storefront is built with Next.js. Customize the UI by modifying the components in the <code>src/components</code> directory and pages in the <code>src/pages</code> directory.</p>

</body>
</html>
