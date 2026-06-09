---
description: Quarkus and LangChain4j coding standards for the Vintage Store app
applyTo: "**/*.java"
---

- Use constructor injection, never field `@Inject`.
- REST resources return `RestResponse<T>`; keep business logic in a service, not the resource.
- Validate every request DTO with Bean Validation (`@NotNull`, `@Email`, etc.).
- Persistence stays in repositories; never call the `EntityManager` from a resource.
- Name LangChain4j AI services `XxxAiService` and place them under an `ai/` package.