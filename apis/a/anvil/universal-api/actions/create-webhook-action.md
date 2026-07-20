# Anvil: Create Webhook Action

Creates a new webhook action in Anvil.

```
POST https://connect.mindcloud.co/v1/universal/anvil/latest/actions/create-webhook-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anvil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anvil/latest/actions/create-webhook-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.action": "string",
  "variables.objectType": "string",
  "variables.objectEid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anvil/latest/actions/create-webhook-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.action": "string",
    "variables.objectType": "string",
    "variables.objectEid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.action` | string | yes | Provide Action for Create Webhook Action. |
| `variables.objectType` | string | yes | Provide Object Type for Create Webhook Action. |
| `variables.objectEid` | string | yes | Provide Object EID for Create Webhook Action. |
| `variables.config` | object | no | Provide Config for Create Webhook Action. |
| `variables.webhookEid` | string | no | Provide Webhook EID for Create Webhook Action. |
| `variables.organizationEid` | string | no | Provide Organization EID for Create Webhook Action. |
| `variables.url` | string | no | Provide URL for Create Webhook Action. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Anvil API returns.

## Native endpoint

Through the native Anvil API, this operation is `POST /` (base URL `https://graphql.useanvil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-action.md) for the provider-specific parameters and requirements.

