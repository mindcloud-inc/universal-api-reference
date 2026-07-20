# Confluent: Create Service Account

Creates a new service account in Confluent Cloud.

```
POST https://connect.mindcloud.co/v1/universal/confluent/latest/actions/create-service-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/confluent/latest/actions/create-service-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "displayName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/confluent/latest/actions/create-service-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "displayName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `displayName` | string | yes | The name of the service account. |
| `description` | string | no | A description of how this service account is used. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignedResourceOwner` | string | no | The resource_id of the principal who will be assigned resource owner on the created service account. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiVersion": "string",
      "description": "string",
      "displayName": "Ava Chen",
      "id": "string",
      "kind": "string",
      "metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiVersion` | string |  |
| `description` | string |  |
| `displayName` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `metadata` | object |  |

## Native endpoint

Through the native Confluent API, this operation is `POST /iam/v2/service-accounts` (base URL `https://api.confluent.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-service-account.md) for the provider-specific parameters and requirements.

