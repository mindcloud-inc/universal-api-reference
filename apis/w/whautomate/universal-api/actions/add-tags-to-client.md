# Whautomate: Add Tags to Client

Updates an existing client in Whautomate by adding tags.

```
PUT https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/add-tags-to-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whautomate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/add-tags-to-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": "string",
  "tags[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/add-tags-to-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": "string",
    "tags[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | yes |  |
| `tags[]` | array<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native Whautomate API, this operation is `POST /v1/clients/{{clientId}}/tags/add` (base URL `https://api.whautomate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-tags-to-client.md) for the provider-specific parameters and requirements.

