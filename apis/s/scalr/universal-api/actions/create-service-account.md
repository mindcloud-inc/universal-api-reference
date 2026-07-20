# Scalr: Create Service Account

Creates a new service account in Scalr.

```
POST https://connect.mindcloud.co/v1/universal/scalr/latest/actions/create-service-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scalr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scalr/latest/actions/create-service-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.attributes.name": "Ava Chen",
  "data.relationships.account.data.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scalr/latest/actions/create-service-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.attributes.name": "Ava Chen",
    "data.relationships.account.data.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.attributes.name` | string | yes | Service account name. |
| `data.attributes.description` | string | no | Service account description. |
| `data.attributes.status` | string | no | Service account status. |
| `data.relationships.account.data.id` | string | yes | Related account ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Scalr API returns.

## Native endpoint

Through the native Scalr API, this operation is `POST /service-accounts` (base URL `https://mindcloud.scalr.io/api/iacp/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-service-account.md) for the provider-specific parameters and requirements.

