# Guiding Principles

These principles establish the foundation for all services and libraries.

* **Clean Code**: Code must be easy to read, understand, and maintain.
* **SOLID principles**: Design software that is more maintainable, robust, scalable, and easier to understand.
* **Clarity over cleverness**: Always prefer readable, explicit code.
* **Secure by default**: Mandates validating all inputs, applying the principle of least privilege, and ensuring no secrets are stored directly in code.
* **Security Standards**: Follow Mitrai Secure Coding standards and the OWASP top 10 checklist and assessment.
* **12-Factor & Cloud-native**: Services must employ stateless processes, externalized configuration, and disposability.
* **Testable & Observable**: Implement unit and integration tests, and include metrics, traces, and structured logs.
* **Fail fast, degrade gracefully**: Use mechanisms like timeouts, retries, circuit breakers, and bulkheads.
* **Small, cohesive modules**: Modules should adhere to a single responsibility, have clear boundaries, and be easy to test and maintain.