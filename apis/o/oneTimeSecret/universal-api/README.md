# <img src="https://images.mindcloud.co/apps/icons/onetime-logo-md_1777567903725.png" alt="One-Time Secret logo" width="28" height="28"> One-Time Secret: Universal API

Create, reveal, track, and burn self-destructing secret links with Onetime Secret's current JSON API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oneTimeSecret/latest
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://onetimesecret.com
- **Vendor API docs:** https://docs.onetimesecret.com/en/rest-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Receipts](actions/v2-list-receipts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-list-receipts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Locale

| Action | Method | Description |
| --- | --- | --- |
| [Get Supported Locales](actions/v2-get-supported-locales.md) | GET | Retrieves supported locales from One-Time Secret. |

### Receipt

| Action | Method | Description |
| --- | --- | --- |
| [Burn Receipt Secret](actions/v2-burn-secret.md) | DELETE | Deletes a secret from One-Time Secret by receipt identifier. |
| [Guest Burn Secret](actions/v2-guest-burn-secret.md) | DELETE | Deletes a guest secret from One-Time Secret by receipt identifier. |
| [Guest Show Receipt](actions/v2-guest-show-receipt.md) | GET | Retrieves a guest receipt from One-Time Secret by identifier. |
| [List Receipts](actions/v2-list-receipts.md) | GET | Retrieves recent secret receipts from One-Time Secret. |
| [Private Burn Secret](actions/v2-private-burn-secret.md) | DELETE | Deletes a private secret from One-Time Secret by receipt identifier. |
| [Private List Receipts](actions/v2-private-list-receipts.md) | GET | Retrieves recent private secret receipts from One-Time Secret. |
| [Private Show Receipt](actions/v2-private-show-receipt.md) | GET | Retrieves a private receipt from One-Time Secret by identifier. |
| [Private Update Receipt](actions/v2-private-update-receipt.md) | PUT | Updates a private receipt in One-Time Secret. |
| [Show Receipt](actions/v2-show-receipt.md) | GET | Retrieves a secret receipt from One-Time Secret by identifier. |
| [Update Receipt](actions/v2-update-receipt.md) | PUT | Updates a secret receipt in One-Time Secret. |

### Secret

| Action | Method | Description |
| --- | --- | --- |
| [Conceal Secret](actions/v2-conceal-secret.md) | POST | Creates a new secret from provided content in One-Time Secret. |
| [Generate Secret](actions/v2-generate-secret.md) | POST | Creates a new secret with a generated value in One-Time Secret. |
| [Guest Conceal Secret](actions/v2-guest-conceal-secret.md) | POST | Creates a guest secret from provided content in One-Time Secret. |
| [Guest Generate Secret](actions/v2-guest-generate-secret.md) | POST | Creates a new guest secret with a generated value in One-Time Secret. |
| [Guest Reveal Secret](actions/v2-guest-reveal-secret.md) | GET | Reveals and consumes a guest secret from One-Time Secret by identifier. |
| [Guest Show Secret](actions/v2-guest-show-secret.md) | GET | Retrieves guest secret metadata from One-Time Secret by identifier. |
| [Reveal Secret](actions/v2-reveal-secret.md) | GET | Reveals and consumes a secret from One-Time Secret by identifier. |
| [Show Secret](actions/v2-show-secret.md) | GET | Retrieves secret metadata from One-Time Secret by identifier. |

### Secret Status

| Action | Method | Description |
| --- | --- | --- |
| [List Secret Status](actions/v2-list-secret-status.md) | GET | Retrieves statuses for multiple secrets in One-Time Secret. |
| [Show Secret Status](actions/v2-show-secret-status.md) | GET | Retrieves a secret's status from One-Time Secret without consuming it. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [System Status](actions/v2-system-status.md) | GET | Retrieves current system status from One-Time Secret. |

### Version

| Action | Method | Description |
| --- | --- | --- |
| [System Version](actions/v2-system-version.md) | GET | Retrieves current system version from One-Time Secret. |

