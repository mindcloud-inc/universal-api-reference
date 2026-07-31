# Random User: Native API Reference

A consolidated summary of Random User's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://randomuser.me/documentation
- **API base URL:** `https://randomuser.me`

## Authentication

### No authentication

Random User Generator is public and does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://randomuser.me/documentation)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 250 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Random Users](actions/generate-random-users.md) | `GET /api/` | [docs](https://randomuser.me/documentation) |
