# xAI: Retrieve Response

Retrieves a response from the xAI API.

```
GET https://connect.mindcloud.co/v1/universal/xAI/latest/actions/retrieve-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xAI/latest/actions/retrieve-response?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xAI/latest/actions/retrieve-response?${params}`, {
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
| `response_id` | string | no | Response ID returned by Create Response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "model": "string",
      "object": "string",
      "output": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `model` | string |  |
| `object` | string |  |
| `output` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native xAI API, this operation is `GET /responses/:response_id` (base URL `https://api.x.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-response.md) for the provider-specific parameters and requirements.

