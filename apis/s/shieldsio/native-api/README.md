# Shields.io: Native API Reference

A consolidated summary of Shields.io's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://shields.io/docs/
- **API base URL:** `https://img.shields.io`

## Authentication

### No authentication

Public unauthenticated Shields.io badge endpoints.

This API does not require request authentication.

[Official authentication documentation](https://shields.io/docs/)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Dynamic JSON Badge](actions/generate-dynamic-json-badge.md) | `GET /badge/dynamic/json` | [docs](https://shields.io/badges/dynamic-json-badge) |
| [Generate Dynamic Regex Badge](actions/generate-dynamic-regex-badge.md) | `GET /badge/dynamic/regex` | [docs](https://shields.io/badges/dynamic-regex-badge) |
| [Generate Dynamic TOML Badge](actions/generate-dynamic-toml-badge.md) | `GET /badge/dynamic/toml` | [docs](https://shields.io/badges/dynamic-toml-badge) |
| [Generate Dynamic XML Badge](actions/generate-dynamic-xml-badge.md) | `GET /badge/dynamic/xml` | [docs](https://shields.io/badges/dynamic-xml-badge) |
| [Generate Dynamic YAML Badge](actions/generate-dynamic-yaml-badge.md) | `GET /badge/dynamic/yaml` | [docs](https://shields.io/badges/dynamic-yaml-badge) |
| [Generate Endpoint Badge](actions/generate-endpoint-badge.md) | `GET /endpoint` | [docs](https://shields.io/badges/endpoint-badge) |
| [Generate Static Badge](actions/generate-static-badge.md) | `GET /badge/:badgeContent` | [docs](https://shields.io/badges/static-badge) |
