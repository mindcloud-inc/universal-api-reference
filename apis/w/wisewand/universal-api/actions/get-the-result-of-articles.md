# Wisewand: Get the result of articles

Retrieves an article result from Wisewand.

```
GET https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-the-result-of-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wisewand `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-the-result-of-articles?connectionId=$CONNECTION_ID&id=test-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "test-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-the-result-of-articles?${params}`, {
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
| `id` | string | yes | Wisewand path parameter `id`. Default: `test-id`. |
| `outputId` | string | no | Wisewand query parameter `outputId`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "all_outputs": [
        {}
      ],
      "created_at": "string",
      "id": "string",
      "input": {},
      "output": {},
      "status": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `all_outputs` | array<object> |  |
| `created_at` | string |  |
| `id` | string |  |
| `input` | object |  |
| `output` | object |  |
| `status` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Wisewand API, this operation is `GET /v1/articles/:id/output` (base URL `https://api.wisewand.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-the-result-of-articles.md) for the provider-specific parameters and requirements.

