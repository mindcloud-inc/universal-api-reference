# Quota usage for one account with ConnectSafely

How much of each rate-limited action this account has spent in the current window. `used` counts every call made through the ConnectSafely API — your own API/MCP calls as well as anything ConnectSafely runs for you — so this is the way to spot an agent burning a quota you did not expect.

A fast, database-only read: it makes no LinkedIn call and consumes none of the quotas it reports, so it is safe to poll.

`limit` is the ceiling ConnectSafely enforces (calls are rejected with 429 at this value); `linkedinLimit` is LinkedIn's own higher ceiling, for context. `window` is `daily` (resets midnight UTC) or `weekly` (resets Monday midnight UTC).

## Endpoint

- **Method:** `GET`
- **Path:** `/account/:accountId/quota`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Quota usage for one account](https://connectsafely.ai/docs/api/linkedin-account/get-account-accountid-quota-get-account-quota)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | param | `string` | yes | LinkedIn account id (24-character Mongo ObjectId). Must be an account you own or one shared with you through a workspace. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | `string` |  |
| `quotas` | `array` |  |
| `quotas[].feature` | `string` | Action name, e.g. PROFILE_VIEW, COMMENT, CONNECT, SEARCH_PEOPLE |
| `quotas[].window` | `list` |  |
| `quotas[].used` | `number` | Calls made on this account in the current window (all sources) |
| `quotas[].limit` | `number` | Ceiling ConnectSafely enforces — 429 at this value |
| `quotas[].linkedinLimit` | `number` | LinkedIn's own higher ceiling, for context only |
| `quotas[].remaining` | `number` | limit minus used, floored at 0 |
| `quotas[].limitReached` | `boolean` | True when LinkedIn returned 429 for this feature in the current window |
| `quotas[].limitReachedAt` | `date` |  |
| `quotas[].resetAt` | `date` | When this window resets |

### Example response

```json
{
  "accountId": "60d21b4667d0d8992e610c85",
  "quotas": [
    {
      "feature": "PROFILE_VIEW",
      "window": "daily",
      "used": 118,
      "limit": 120,
      "linkedinLimit": 150,
      "remaining": 2,
      "limitReached": false,
      "limitReachedAt": null,
      "resetAt": "2026-08-28 00:00:00+00:00"
    },
    {
      "feature": "CONNECT",
      "window": "weekly",
      "used": 12,
      "limit": 90,
      "linkedinLimit": 100,
      "remaining": 78,
      "limitReached": false,
      "limitReachedAt": null,
      "resetAt": "2026-09-01 00:00:00+00:00"
    }
  ]
}
```

## Error status codes

`401`, `403`, `404`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
