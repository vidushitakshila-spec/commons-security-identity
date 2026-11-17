# commons-security-identity
1. Problem statement: Services struggle with decentralized user context propagation, inconsistent JWT/OAuth2 claim extraction, and lack of unified security context holders across asynchronous threads.

2. Concepts and terminology: Security Context, Principal, JWT Claims, ThreadLocal context propagation, Reactive/MVC context switching.

3. Available technologies / algorithms: Spring Security, Nimbus JOSE + JWT, JJWT, JCA (Java Cryptography Architecture).

4. When to use what: Use whenever a microservice needs to extract, validate, or propagate user identities, roles, and enterprise scopes (customer:read:pii).

5. Java APIs and dependencies: spring-boot-starter-security, oauth2-resource-server, jjwt-api.

6. AWS equivalents: AWS Cognito, IAM Principal Context.

7. Architecture patterns: Zero-Trust Context Propagation, Claims-Based Access Control (CBAC), Request Scoped Bean Injection.

8. Security considerations: Guard against token replay attacks; ensure SecurityContextHolder is cleared on thread completion to prevent thread-pool pollution.

9. Implementation examples: Custom JwtAuthenticationConverter mapping custom scopes to Spring GrantedAuthorities.

10. References and further reading: OAuth 2.0 RFC 6749, OWASP Session Management Cheat Sheet.
