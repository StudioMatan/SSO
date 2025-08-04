# Single Sign-On (SSO) Authentication

This project provides an overview of different authentication protocols used for Single Sign-On (SSO), including SAML, OAuth 2.0, and OpenID Connect. It includes use cases, flows, and configuration best practices.

## When to Use

- **SAML**: Ideal for enterprise single sign-on. Users log into a corporate identity provider (e.g., M365) once and access all company apps without re-authentication.
- **OpenID Connect**: A modern authentication protocol built on top of OAuth, focusing on user identity verification using JSON tokens (JWT).
- **OAuth 2.0**: Used for app-to-app permission systems, allowing apps to access other apps on behalf of the user without sharing passwords.

## Protocol Flows

### SAML

1. **SAML Authentication Request**: When accessing an app, a SAML Request is created and redirects the browser to the company's identity provider.
2. **SAML Assertion**: The identity provider generates a SAML Assertion, which is sent back to the app, granting access.
3. **Claims**: Information about the user (e.g., name, email, department) passed in the token.

### OAuth 2.0

- Allows apps to access other apps on behalf of the user without sharing passwords.
- Example Flow:
  1. Slack asks, "Can I access your Jira?"
  2. User logs into Jira and grants read access.
  3. Jira provides Slack with an access token.
  4. Slack uses the token to access data.

### OpenID Connect

- Similar to SAML but uses JSON instead of XML.
- The app redirects the user to the identity provider, which returns a JWT token with identity information.

## Configuration Best Practices

### SAML

- Use signed assertions and encryption when possible.
- Configure proper audience restrictions.
- Set reasonable token expiration.
- Ensure consistent user IDs.

### OAuth

- Use the authorization code flow.
- Implement PKCE for additional security.
- Scope permissions to the least privilege.
- Secure client credentials properly.

## Diagrams

Include any relevant diagrams here.
https://github.com/StudioMatan/SSO/blob/main/SSO.pdf 
---

*Hope you like my diagrams - took me a minute 🤓*
