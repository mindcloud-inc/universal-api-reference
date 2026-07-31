# Harry Potter API: Native API Reference

A consolidated summary of Harry Potter API's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://hp-api.onrender.com/
- **API base URL:** `https://hp-api.onrender.com`

## Authentication

### No authentication

This API does not require request authentication.

[Official authentication documentation](https://hp-api.onrender.com/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Character](actions/get-character.md) | `GET /api/character/:id` | [docs](https://hp-api.onrender.com/) |
| [List Characters](actions/list-characters.md) | `GET /api/characters` | [docs](https://hp-api.onrender.com/) |
| [List Characters by House](actions/list-characters-by-house.md) | `GET /api/characters/house/:house` | [docs](https://hp-api.onrender.com/) |
| [List Spells](actions/list-spells.md) | `GET /api/spells` | [docs](https://hp-api.onrender.com/) |
| [List Staff](actions/list-staff.md) | `GET /api/characters/staff` | [docs](https://hp-api.onrender.com/) |
| [List Students](actions/list-students.md) | `GET /api/characters/students` | [docs](https://hp-api.onrender.com/) |
