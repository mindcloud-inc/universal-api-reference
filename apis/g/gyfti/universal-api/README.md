# <img src="https://images.mindcloud.co/apps/icons/favicon-developer-gyfti-fr-48x48_1777546631784.png" alt="gyfti logo" width="28" height="28"> gyfti: Universal API

Use gyfti to automate gift campaigns, store users, wallet pool updates, and webhook registrations for campaign and store events.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gyfti/latest
- **Category:** Marketing
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.gyfti.fr/
- **Vendor API docs:** https://developer.gyfti.fr/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Credentials](actions/verify-credentials.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/verify-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from gyfti. |

### Campaign Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact to Email Campaign](actions/add-contact-to-email-campaign.md) | POST | Adds a contact to an email campaign in gyfti. |

### New Email Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Register New Email Webhook](actions/register-new-email-webhook.md) | POST | Registers a new email webhook in gyfti. |

### New Order Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Register New Order Webhook](actions/register-new-order-webhook.md) | POST | Registers a new order webhook in gyfti. |

### Order Update Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Register Order Update Webhook](actions/register-order-update-webhook.md) | POST | Registers an order update webhook in gyfti. |

### Postal Campaign Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact to Postal Campaign](actions/add-contact-to-postal-campaign.md) | POST | Adds a contact to a postal campaign in gyfti. |

### Store User

| Action | Method | Description |
| --- | --- | --- |
| [Add or Update Store User](actions/add-or-update-store-user.md) | PUT | Adds or updates a user in gyfti Store. |

### Store User Pool

| Action | Method | Description |
| --- | --- | --- |
| [Add Pool to Store User](actions/add-pool-to-store-user.md) | PUT | Adds a pool to a gyfti Store user. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Verify Credentials](actions/verify-credentials.md) | GET | Verifies gyfti API credentials with an access token. |

