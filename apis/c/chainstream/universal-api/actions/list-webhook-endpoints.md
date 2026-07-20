# Chainstream: List Webhook Endpoints

Retrieves webhook endpoints from Chainstream.

```
GET https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/list-webhook-endpoints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chainstream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/list-webhook-endpoints?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/list-webhook-endpoints?${params}`, {
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
| `limit` | number | no | Number of results per page Default: `100`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `iterator` | string | no | Pagination iterator |
| `order` | string | no | Ordering direction for paginated endpoint listing Default: `descending`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "channels": [
            [
              "string"
            ]
          ],
          "createdAt": "string",
          "description": "string",
          "disabled": true,
          "id": "string",
          "updatedAt": "string",
          "url": "https://example.com"
        }
      ],
      "done": true,
      "iterator": "string",
      "prevIterator": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].channels[]` | array<string> |  |
| `data[].createdAt` | string |  |
| `data[].description` | string |  |
| `data[].disabled` | boolean |  |
| `data[].id` | string |  |
| `data[].updatedAt` | string |  |
| `data[].url` | string |  |
| `done` | boolean |  |
| `iterator` | string |  |
| `prevIterator` | string |  |

## Native endpoint

Through the native Chainstream API, this operation is `GET /v2/webhook/endpoint` (base URL `https://api.chainstream.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-endpoints.md) for the provider-specific parameters and requirements.

