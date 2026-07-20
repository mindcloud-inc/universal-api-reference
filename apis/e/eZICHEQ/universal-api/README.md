# <img src="https://images.mindcloud.co/apps/icons/e-zicheq_1775220780844.png" alt="EZICHEQ logo" width="28" height="28"> EZICHEQ: Universal API

EZICHEQ safety net testing and asset tagging API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eZICHEQ/latest
- **Category:** Support / Field Service
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ezicheq.com
- **Vendor API docs:** https://developer.ezicheq.com/docs/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test Connection](actions/test-connection.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eZICHEQ/latest/actions/test-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves your EZICHEQ account details. |

### Check

| Action | Method | Description |
| --- | --- | --- |
| [Get Check](actions/get-check.md) | GET | Retrieves a certified check from EZICHEQ. |
| [List Checks](actions/list-checks.md) | GET | Retrieves certified checks from EZICHEQ. |

### Checklists

| Action | Method | Description |
| --- | --- | --- |
| [Get Checklist](actions/get-checklist.md) | GET | Retrieves a checklist from EZICHEQ. |
| [List Checklists](actions/list-checklists.md) | GET | Retrieves checklists from EZICHEQ. |

### Item Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Type](actions/get-item-type.md) | GET | Retrieves an item type from EZICHEQ. |
| [List Item Types](actions/list-item-types.md) | GET | Retrieves item types from EZICHEQ. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST | Creates an item in EZICHEQ. |
| [Delete Item](actions/delete-item.md) | DELETE | Deletes an item from EZICHEQ. |
| [Get Item](actions/get-item.md) | GET | Retrieves an item from EZICHEQ. |
| [List Items](actions/list-items.md) | GET | Retrieves items from EZICHEQ. |
| [Update Item](actions/update-item.md) | PUT | Updates an item in EZICHEQ. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [Create Label](actions/create-label.md) | POST |  |
| [Delete Label](actions/delete-label.md) | DELETE |  |
| [Get Label](actions/get-label.md) | GET | Retrieves a label from EZICHEQ. |
| [List Labels](actions/list-labels.md) | GET |  |
| [Update Label](actions/update-label.md) | PUT | Updates a label in EZICHEQ. |

### Self Check

| Action | Method | Description |
| --- | --- | --- |
| [Get Self Check](actions/get-self-check.md) | GET | Retrieves a self check from EZICHEQ. |
| [List Self Checks](actions/list-self-checks.md) | GET | Retrieves self checks from EZICHEQ. |

### Test

| Action | Method | Description |
| --- | --- | --- |
| [Create Test](actions/create-test.md) | POST |  |
| [Delete Test](actions/delete-test.md) | DELETE |  |
| [Update Test](actions/update-test.md) | PUT |  |

### Test Connection

| Action | Method | Description |
| --- | --- | --- |
| [Test Connection](actions/test-connection.md) | GET | Tests your EZICHEQ connection. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from EZICHEQ. |
| [List Users](actions/list-users.md) | GET | Retrieves users from EZICHEQ. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in EZICHEQ. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from EZICHEQ. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from EZICHEQ. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from EZICHEQ. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates a webhook in EZICHEQ. |

