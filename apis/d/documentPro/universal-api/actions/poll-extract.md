# DocumentPro: Poll Extract

Retrieves an extract job result from DocumentPro.

```
GET https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/poll-extract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocumentPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/poll-extract?connectionId=$CONNECTION_ID&request_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/poll-extract?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `request_id` | string | yes | The request_id returned from Run Extract. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "request_id": "string",
      "request_status": "string",
      "response_body": {},
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `request_id` | string |  |
| `request_status` | string |  |
| `response_body` | object |  |
| `updated_at` | string |  |

## Native endpoint

Through the native DocumentPro API, this operation is `GET /files` (base URL `https://api.documentpro.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/poll-extract.md) for the provider-specific parameters and requirements.

