# Arine

Arine is a San Francisco-based healthcare technology company operating an AI-driven medication
intelligence and comprehensive medication management platform for health plans, government payors
and risk-bearing provider organizations. Its four solutions are LUMINATE (high-risk member
management), RESONATE (prescriber analytics), ELEVATE (quality and Star Ratings improvement) and
ELEVATE MTM (medication therapy management).

- Website: https://www.arine.io/
- Blog and resources: https://blog.arine.io/
- Documentation portal (authentication required): https://docs.arine.io/
- Secondary-market listing: https://forgeglobal.com/arine_stock/

## API posture

Arine ships **no public developer program and no publicly available machine-readable API contract**.
Verified by probe on 2026-08-02:

- `https://api.arine.io` is an AWS API Gateway that returns HTTP 403 `ForbiddenException` on every
  probed path, including `/openapi.json`, `/swagger.json`, `/graphql`, `/api-docs` and `/.well-known/*`.
- `https://docs.arine.io` is a Document360 knowledge base with `projectProtectionLevel: 1`; every path
  302-redirects to an OIDC login.
- No OpenAPI, Swagger, GraphQL SDL, AsyncAPI, MCP server, A2A agent card, `security.txt`, SDK, CLI,
  Postman collection or public changelog was found on any Arine host or in npm / PyPI.

Full probe transcript: [`well-known/arine-well-known.yml`](well-known/arine-well-known.yml).

## Artifacts

| Artifact | File |
|---|---|
| Conformance / compliance posture | `conformance/arine-conformance.yml` |
| Domain security (TLS/HSTS/DNSSEC/CAA/SPF/DMARC) | `security/arine-domain-security.yml` |
| Well-known + contract discovery probe | `well-known/arine-well-known.yml` |
| llms.txt | `llms/arine-llms.txt` |

Arine holds HITRUST Risk-based, 2-year (r2) certification for the Arine Platform running in AWS
(<https://blog.arine.io/hitrust>).
