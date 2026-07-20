# HappyScribe: Retrieve Order

Retrieves an order from HappyScribe.

```
GET https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/retrieve-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyScribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/retrieve-order?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/retrieve-order?${params}`, {
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
| `id` | string | yes | The order identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canBeSubmitted": true,
      "details": {},
      "folder_id": 1,
      "id": "string",
      "ingestions": [
        {}
      ],
      "inputs": [
        {}
      ],
      "operations": [
        {}
      ],
      "state": "string",
      "transcriptions": [
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
| `canBeSubmitted` | boolean |  |
| `details` | object |  |
| `folder_id` | number |  |
| `id` | string |  |
| `ingestions` | array<object> |  |
| `inputs` | array<object> |  |
| `operations` | array<object> |  |
| `state` | string |  |
| `transcriptions` | array<object> |  |

## Native endpoint

Through the native HappyScribe API, this operation is `GET /orders/:id` (base URL `https://www.happyscribe.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-order.md) for the provider-specific parameters and requirements.

