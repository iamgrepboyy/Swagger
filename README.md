# Swagger API Reference

This repository contains a Swagger/OpenAPI 2.0 specification for the Jamf Pro Classic API resource documentation. It is intended as a reference and proof-of-concept artifact for exploring and working with the Jamf Pro `JSSResource` endpoints.

## Repository contents

- `swagger.yaml` — the main API definition in YAML format
- `swagger.json` — the same API definition in JSON format
- `README.md` — project documentation

## Overview

The included specification describes a legacy API surface for Jamf Pro resources, including:

- accounts and user/group lookup endpoints
- activation code management
- advanced search resources
- building and category management
- class and computer application endpoints
- BYOD profile and site-based queries
- many additional Jamf Pro resource routes

The OpenAPI document indicates:

- Swagger/OpenAPI version: `2.0`
- Base path: `/JSSResource/`
- Supported media types: `application/xml`, `application/json`
- Authentication: HTTP Basic Auth (`basicAuth`)

## Why this repository exists

This project is useful for:

- reviewing Jamf Pro API structure visually in Swagger UI
- importing the spec into tools like Postman, Insomnia, or Stoplight
- generating API clients or documentation
- understanding the available resource paths and operations

This is a specification/documentation project, not a full server or application implementation.

## Quick start

### View the API spec

Open `swagger.yaml` in one of the following tools:

- Swagger Editor
- Swagger UI
- Redoc
- Postman (OpenAPI import)

You can also use the JSON version in `swagger.json` if your tooling prefers JSON.

### Example usage

The API uses basic authentication and a Jamf Pro base URL. A typical request pattern is:

```bash
curl -u "username:password" \
  -H "Accept: application/json" \
  "https://your-jamf-instance.example.com/JSSResource/accounts"
```

## Important notes

- This is a reference/PoC API document for Jamf Pro Classic endpoints.
- The API is built around the `/JSSResource/` path prefix.
- Requests and responses may be returned in either XML or JSON, depending on the client and endpoint.
- Basic authentication is expected for protected resources.

## Documentation status

This project currently provides the raw Swagger/OpenAPI definition and minimal project documentation. It does not include a custom app frontend, CI workflow, or additional code implementation.

## License

No explicit license was found in the repository root. If you plan to publish or redistribute this specification, consider adding a suitable open-source license such as MIT or Apache 2.0.

## Contributing

If you want to improve this repository, you can:

- add a richer API description section
- add example requests and sample responses
- provide a visual documentation page
- clean up the generated spec and improve naming consistency
