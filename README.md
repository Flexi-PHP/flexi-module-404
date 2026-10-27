# 404 Module

The 404 module provides a customizable page for unmatched routes. Its `RouteNotFoundListener` stores the requested path in the session and returns a redirect to `/not-found`; the controller renders the configured HTML page with status 404 and logs the event.

## Dependencies and configuration

The configured services require the Session, Logging, and UI modules. Route, listener, and service registrations are in `Config/routes.json`, `Config/listeners.json`, and `Config/services.json`. The page template is under `Infrastructure/UI/Templates/404.html`.

Install `cubadevops/flexi-module-404` and activate `404` after its declared dependencies. It supports PHP 7.4+, Flexi Core `^3.2`, and `flexi/contracts` `^5.2.1`.

The UI renderer currently performs literal substitution without automatic escaping. Treat the template and interpolated values as trusted, or use a renderer with context-aware escaping for untrusted input.
