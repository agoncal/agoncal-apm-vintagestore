---
name: rest-endpoint
description: Use when adding or changing a Quarkus REST endpoint in the Vintage Store app. Scaffolds the resource, DTO, and test following Vintage Store conventions.
---

# Quarkus REST endpoint

Follow these steps when the user asks for a new endpoint.

## Steps
1. Create `<Entity>Resource` under `src/main/java/.../rest/`.
2. Annotate the class with `@Path` and inject the repository through the constructor.
3. Expose CRUD methods returning `RestResponse<T>` with `@GET`, `@POST`, `@PUT`, `@DELETE`.
4. Add a `<Entity>DTO` record and a dedicated mapper; never expose entities directly.
5. Generate a `@QuarkusTest` covering the happy path and one validation failure.

## Conventions
- Constructor injection only.
- Bean Validation on every request DTO.
- Keep the resource thin; delegate to a service.