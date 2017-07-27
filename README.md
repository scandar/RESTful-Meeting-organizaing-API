<h2>RESTful Meeting organizing API</h2>

<p>you can start by running</p>
<pre>composer install</pre>
create a DB table and configure it in the <pre>.env</pre> file then run:
<pre>php artisan migrate</pre>
<hr>
<h3>API routes:</h3> 

<div class="route">
	<p>Sign up a user: <pre>/api/v1/user</pre></p> 
	<p>Method: <pre>POST</pre></p>
	<p>params: <pre>name, email, password</pre></p>
</div>
<hr>

<div class="route">
	<p>sign in: <pre>/api/v1/user/signin</pre></p> 
	<p>Method: <pre>POST</pre></p>
	<p>params: <pre>email, password</pre></p>
</div>
<hr>

<div class="route">
	<p>View all meetings: <pre>/api/v1/meeting</pre></p> 
	<p>Method: <pre>GET</pre></p>
</div>
<hr>

<div class="route">
	<p>view specific meeting: <pre>/api/v1/meeting/(id)</pre></p> 
	<p>Method: <pre>GET</pre></p>
</div>
<hr>

<div class="route">
	<p>Add meeting: <pre>/api/v1/meeting</pre></p> 
	<p>Method: <pre>POST</pre></p>
	<p>params: <pre>title, description, time</pre></p>
	<p>time must be in the format "YmdHie" e.g: 201707241330CET</p>
</div>
<hr>

<div class="route">
	<p>update meeting: <pre>/api/v1/meeting/(id)</pre></p> 
	<p>Method: <pre>PATCH</pre></p>
	<p>params: <pre>title, description, time</pre></p>
	<p>time must be in the format "YmdHie" e.g: 201707241330CET</p>
</div>
<hr>

<div class="route">
	<p>Delete meeting: <pre>/api/v1/meeting/(id)</pre></p> 
	<p>Method: <pre>DELETE</pre></p>
</div>
<hr>


<div class="route">
	<p>Register a user for a meeting: <pre>/api/v1/meeting/registration</pre></p> 
	<p>Method: <pre>POST</pre></p>
	<p>params: <pre>meeting_id, user_id</pre></p>
</div>
<hr>

<div class="route">
	<p>Unregister a user from a meeting: <pre>/api/v1/meeting/registration/(meeting_id)</pre></p> 
	<p>Method: <pre>DELETE</pre></p>
	<p>params: <pre>meeting_id, user_id</pre></p>
</div>
