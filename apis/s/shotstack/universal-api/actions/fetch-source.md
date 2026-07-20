# Shotstack: Fetch Source



```
POST https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/fetch-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shotstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/fetch-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/fetch-source', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | The Shotstack request body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.id` | string | Queued source identifier. |
| `data.type` | string | Resource type for the queued source. |

## Native endpoint

Through the native Shotstack API, this operation is `POST /ingest/v1/sources` (base URL `https://api.shotstack.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-source.md) for the provider-specific parameters and requirements.

