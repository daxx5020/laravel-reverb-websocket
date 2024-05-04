<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>

<h1>Laravel 11 WebSocket Project Setup Guide</h1>

<img src="https://github.com/daxx5020/laravel-reverb-websocket/assets/121967015/c454c22f-d439-4dd4-b952-fbda2abbef20" alt="Laravel Logo" style="width: 1000px; height: auto;">

<h2>Step 1: Copy Environment File</h2>

<p>Copy the <code>.env.example</code> file to <code>.env</code>:</p>

<pre><code>cp .env.example .env</code></pre>

<h2>Step 2: Install Dependencies</h2>

<p>Install the project dependencies using Composer:</p>

<pre><code>composer install</code></pre>

<h2>Step 3: Generate Application Key</h2>

<p>Generate the application key:</p>

<pre><code>php artisan key:generate</code></pre>

<h2>Step 4: Configure Database</h2>

<p>Create a MySQL database and set the database credentials in the <code>.env</code> file:</p>

<pre><code>DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE="&lt;database_name&gt;"
DB_USERNAME="&lt;username&gt;"
DB_PASSWORD="&lt;password&gt;"</code></pre>

<h2>Step 5: Setup Reverb Credentials</h2>

<p>Configure Reverb credentials in the <code>.env</code> file:</p>

<pre><code>BROADCAST_CONNECTION=reverb

REVERB_APP_ID=
REVERB_APP_KEY=
REVERB_APP_SECRET=
REVERB_HOST="localhost"
REVERB_PORT=8080
REVERB_SCHEME=http

VITE_REVERB_APP_KEY="${REVERB_APP_KEY}"
VITE_REVERB_HOST="${REVERB_HOST}"
VITE_REVERB_PORT="${REVERB_PORT}"
VITE_REVERB_SCHEME="${REVERB_SCHEME}"</code></pre>

<h2>Step 6: Optimize Application Cache</h2>

<p>Optimize the application cache:</p>

<pre><code>php artisan optimize</code></pre>

<h2>Step 7: Run Migrations</h2>

<p>Run the database migrations:</p>

<pre><code>php artisan migrate:fresh</code></pre>

<h2>Step 8: Install NPM Dependencies</h2>

<p>Install the NPM dependencies:</p>

<pre><code>npm install</code></pre>

<h2>Step 9: Build Assets</h2>

<p>Build the assets:</p>

<pre><code>npm run build</code></pre>

<h2>Step 10: [Optional] Watch Assets for Changes</h2>

<p>For development, you can watch the assets for changes:</p>

<pre><code>npm run dev</code></pre>

<h2>Step 11: Start WebSocket Server</h2>

<p>Start the WebSocket server:</p>

<pre><code>php artisan reverb:start</code></pre>

<h2>Step 12: Start Listening to Queue Jobs</h2>

<p>Start listening to Queue jobs:</p>

<pre><code>php artisan queue:listen</code></pre>

<h2>Step 13: Start Development Server</h2>

<p>Start the development server using the following command or configure a virtual host:</p>

<pre><code>php artisan serve</code></pre>

</body>
</html>
