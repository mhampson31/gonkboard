# gonkboard
A dashboard for Authentik-supported apps

Gonkboard is a dashboard that integrates with Authentik, automatically displaying the logged-in user's list of applications. This is all still very incomplete.

Authentik does have a perfectly good dashboard built in. So why Gonkboard? Two reasons: First, in practical terms, I wanted a dashboard I could run on a different subdomain than Authentik. And second, this project is a personal learning exercise, to develop my understanding of the Rust ecosystem. Other features are planned.

It's not likely to work out of the box with other auth providers -- it expects to be able to make requests against an Authentik API, and deserialize the response according to its schema.

What works?
* Login/logout, althout logout is probably naive
* Retrieving user data, including applications the user can access, from Authentik
* Displaying the applications to the user

Future work:
* DB backend
* User-added bookmark links
* Substantial prettification

Setup:
1. Add a new OAuth2 app in your Authentik environment for Gonkboard
2. Configure the .env file for Gonkboard with the appropriate fields