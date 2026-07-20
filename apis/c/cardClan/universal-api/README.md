# <img src="https://images.mindcloud.co/apps/icons/clip-path-group-1_1781292073214.png" alt="CardClan logo" width="28" height="28"> CardClan: Universal API

Send personalized digital cards and automate card delivery from CardClan workspaces.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cardClan/latest
- **Category:** Marketing
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cardclan.io/
- **Vendor API docs:** https://docs.cardclan.io/api-reference/integration/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Validate Authentication](actions/validate-authentication.md) | GET | Retrieves user details for a valid CardClan integration key. |

### Card

| Action | Method | Description |
| --- | --- | --- |
| [List Cards](actions/list-cards.md) | GET | Retrieves cards from a CardClan workspace. |

### Carddelivery

| Action | Method | Description |
| --- | --- | --- |
| [Send Card](actions/send-card.md) | POST | Sends a personalized CardClan card by email. |

### Carddetail

| Action | Method | Description |
| --- | --- | --- |
| [Get Card Details](actions/get-card-details.md) | GET | Retrieves details for a CardClan card. |

### Cardurl

| Action | Method | Description |
| --- | --- | --- |
| [Get Card URL](actions/get-card-url.md) | GET | Generates a personalized CardClan card URL without sending email. |

### Emailaccount

| Action | Method | Description |
| --- | --- | --- |
| [List Email Accounts](actions/list-email-accounts.md) | GET | Retrieves email accounts configured in CardClan workspaces. |

### Integrationconfig

| Action | Method | Description |
| --- | --- | --- |
| [Create Integration Configuration](actions/create-integration-configuration.md) | POST | Creates a CardClan integration configuration for a card workflow. |
| [Get Configuration by Card](actions/get-configuration-by-card.md) | GET | Retrieves a CardClan integration configuration for a card. |
| [Get Integration Configuration](actions/get-integration-configuration.md) | GET | Retrieves a CardClan integration configuration by ID. |

### Workflowcard

| Action | Method | Description |
| --- | --- | --- |
| [List Cards With Workflows](actions/list-cards-with-workflows.md) | GET | Retrieves CardClan cards with active integration workflows. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces accessible to the CardClan integration. |

