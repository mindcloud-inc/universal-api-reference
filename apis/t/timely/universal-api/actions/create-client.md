# Timely: Create Client

Creates a client in Timely.

```
POST https://connect.mindcloud.co/v1/universal/timely/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timely/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "client": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timely/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "client": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | Account ID for the client you want to create |
| `client` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "color": "string",
      "external_id": "string",
      "external_references": {
        "connection_id": 1,
        "id": 1,
        "provider_id": "string",
        "provider_type": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "url": "https://example.com"
      },
      "id": 1,
      "name": "Ava Chen",
      "tic": {
        "external_url": "https://example.com",
        "tool_id": "string",
        "uri": "string"
      },
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `color` | string |  |
| `external_id` | string |  |
| `external_references` | array<object> |  |
| `external_references.connection_id` | number |  |
| `external_references.id` | number |  |
| `external_references.provider_id` | string |  |
| `external_references.provider_type` | string |  |
| `external_references.updated_at` | date |  |
| `external_references.url` | string |  |
| `id` | number |  |
| `name` | string |  |
| `tic` | object |  |
| `tic.external_url` | string |  |
| `tic.tool_id` | string |  |
| `tic.uri` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Timely API, this operation is `POST /1.1/{account_id}/clients` (base URL `https://api.timelyapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

