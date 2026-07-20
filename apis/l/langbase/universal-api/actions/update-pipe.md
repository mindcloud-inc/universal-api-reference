# Langbase: Update Pipe



```
PUT https://connect.mindcloud.co/v1/universal/langbase/latest/actions/update-pipe
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/langbase/latest/actions/update-pipe" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pipeName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langbase/latest/actions/update-pipe', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pipeName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pipeName` | string | yes | Pipe name to update. |
| `description` | string | no | Updated pipe description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKey": "string",
      "description": "string",
      "name": "Ava Chen",
      "ownerLogin": "string",
      "status": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKey` | string |  |
| `description` | string |  |
| `name` | string |  |
| `ownerLogin` | string |  |
| `status` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Langbase API, this operation is `POST v1/pipes/:pipeName` (base URL `https://api.langbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-pipe.md) for the provider-specific parameters and requirements.

