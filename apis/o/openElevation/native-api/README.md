# Open-Elevation: Native API Reference

A consolidated summary of Open-Elevation's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://github.com/Jorl17/open-elevation/blob/master/docs/api.md
- **API base URL:** `https://api.open-elevation.com`

## Authentication

### No authentication

Open-Elevation public lookup requests do not require authentication.

This API does not require request authentication.

[Official authentication documentation](https://github.com/Jorl17/open-elevation/blob/master/docs/api.md)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Look Up Elevation](actions/look-up-elevation.md) | `GET /api/v1/lookup` | [docs](https://github.com/Jorl17/open-elevation/blob/master/docs/api.md#get-apiv1lookup) |
| [Look Up Elevations From Body](actions/look-up-elevations-from-body.md) | `POST /api/v1/lookup` | [docs](https://github.com/Jorl17/open-elevation/blob/master/docs/api.md#post-apiv1lookup) |
