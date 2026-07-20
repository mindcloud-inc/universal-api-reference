# fal.ai: Get Pricing

Retrieves model endpoint pricing from fal.ai.

```
GET https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-pricing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fal.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-pricing?connectionId=$CONNECTION_ID&endpointId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endpointId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-pricing?${params}`, {
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
| `endpointId` | string | yes | Exact fal.ai endpoint ID to price. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "has_more": true,
      "next_cursor": "string",
      "prices": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `has_more` | boolean |  |
| `next_cursor` | string |  |
| `prices` | array<object> |  |

## Native endpoint

Through the native fal.ai API, this operation is `GET /models/pricing` (base URL `https://api.fal.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pricing.md) for the provider-specific parameters and requirements.

