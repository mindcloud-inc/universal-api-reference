# fal.ai: List Serverless Requests By Endpoint

Retrieves requests for fal.ai serverless endpoints.

```
GET https://connect.mindcloud.co/v1/universal/falai/latest/actions/list-serverless-requests-by-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fal.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/falai/latest/actions/list-serverless-requests-by-endpoint?connectionId=$CONNECTION_ID&endpointId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endpointId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/falai/latest/actions/list-serverless-requests-by-endpoint?${params}`, {
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
| `endpointId` | string | yes | Exact fal.ai endpoint ID to inspect requests for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "has_more": true,
      "items": [
        {}
      ],
      "next_cursor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `has_more` | boolean |  |
| `items` | array<object> |  |
| `next_cursor` | string |  |

## Native endpoint

Through the native fal.ai API, this operation is `GET /serverless/requests/by-endpoint` (base URL `https://api.fal.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-serverless-requests-by-endpoint.md) for the provider-specific parameters and requirements.

