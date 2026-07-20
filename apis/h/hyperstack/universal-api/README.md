# <img src="https://images.mindcloud.co/apps/icons/images-13_1774633574888.png" alt="Hyperstack Certificates logo" width="28" height="28"> Hyperstack Certificates: Universal API

Manage Hyperstack credentials, groups, recipients, and webhook subscriptions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hyperstack/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://thehyperstack.com
- **Vendor API docs:** https://thehyperstack.com/docs/api-guide/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Authenticate](actions/authenticate.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/authenticate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | GET |  |

### Credential

| Action | Method | Description |
| --- | --- | --- |
| [Generate Credential Draft](actions/generate-credential-draft.md) | POST |  |
| [Issue Credential](actions/issue-credential.md) | POST |  |
| [List All Credentials](actions/list-all-credentials.md) | GET |  |
| [Publish Credential](actions/publish-credential.md) | PUT |  |
| [Search Credentials](actions/search-credentials.md) | GET |  |
| [Update Credential](actions/update-credential.md) | PUT |  |
| [View Credential](actions/view-credential.md) | GET |  |

### Credential Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Credential Group](actions/create-credential-group.md) | POST |  |
| [List All Groups](actions/list-all-groups.md) | GET |  |
| [Search Groups](actions/search-groups.md) | GET |  |
| [Update Credential Group](actions/update-credential-group.md) | PUT |  |
| [View Credential Group](actions/view-credential-group.md) | GET |  |

### Recipient

| Action | Method | Description |
| --- | --- | --- |
| [Update Recipient](actions/update-recipient.md) | PUT |  |

### Webhook Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Subscribe to Webhook](actions/subscribe-to-webhook.md) | POST |  |
| [Unsubscribe from Webhook](actions/unsubscribe-from-webhook.md) | DELETE |  |

