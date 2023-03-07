Email on user creation - Keycloak Provider
==========================================

This provider is used to email a particular email address every time a new user is registered in your realm in Keycloak.

Why? Users can automatically 'register' in Keycloak by logging in via an IdP and we would like to know which users are authenticating this way are accessing our services.

This may also be useful if you're doing some debugging and would like emails anyway - or just act as another example of an EventProviderListener implementation.

How to use
----------

Build a .jar with Maven - `mvn package`

Copy this to your providers directory (e.g. `/opt/keycloak/providers/`)

Edit your `keycloak.conf` (e.g. `/opt/keycloak/conf/keycloak.conf`) with the email address you'd like to use as follows:

`spi-events-listener-email-on-user-creation-email-address=example@example.com`

Then, you need to go to the 'Events' settings in your realm, and add this event listener there.