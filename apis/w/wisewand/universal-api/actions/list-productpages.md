# Wisewand: List productpages

Retrieves product pages from your Wisewand workspace.

```
GET https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/list-productpages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wisewand `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/list-productpages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/list-productpages?${params}`, {
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
| `search` | string | no | Wisewand query parameter `search`. |
| `maker` | string | no | Wisewand query parameter `maker`. |
| `status` | string | no | Wisewand query parameter `status`. |
| `projectId` | string | no | Wisewand query parameter `projectId`. |
| `persona` | string | no | Wisewand query parameter `persona`. |
| `author` | string | no | Wisewand query parameter `author`. |
| `category` | string | no | Wisewand query parameter `category`. |
| `published` | string | no | Wisewand query parameter `published`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "items": [
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
| `count` | number |  |
| `items` | array<object> |  |

## Native endpoint

Through the native Wisewand API, this operation is `GET /v1/productpages/` (base URL `https://api.wisewand.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-productpages.md) for the provider-specific parameters and requirements.

