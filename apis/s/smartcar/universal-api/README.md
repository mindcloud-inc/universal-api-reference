# <img src="https://images.mindcloud.co/apps/icons/smartcar_1777305074321.png" alt="Smartcar logo" width="28" height="28"> Smartcar: Universal API

Access connected vehicle data, connections, and remote commands across supported OEM brands.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/smartcar/latest
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://smartcar.com/
- **Vendor API docs:** https://smartcar.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Connections](actions/list-connections.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartcar/latest/actions/list-connections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [List Connections](actions/list-connections.md) | GET | Retrieves connections from Smartcar. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Get Connection](actions/get-connection.md) | GET | Retrieves a connection from Smartcar. |
| [Remove Connection](actions/remove-connection.md) | DELETE | Deletes an existing connection from Smartcar. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a new subscription in Smartcar. |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves a subscription from Smartcar. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from Smartcar. |
| [Remove Subscription](actions/remove-subscription.md) | DELETE | Deletes an existing subscription from Smartcar. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Remove User](actions/remove-user.md) | DELETE | Deletes an existing user from Smartcar. |

### Vehicle

| Action | Method | Description |
| --- | --- | --- |
| [Compatible Vehicles](actions/compatible-vehicles.md) | GET | Retrieves compatible vehicles from Smartcar. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook endpoint from Smartcar. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhook endpoints from Smartcar. |

