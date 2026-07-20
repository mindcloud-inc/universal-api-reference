# Wisewand: Get entity counts summary

Retrieves entity count summaries from your Wisewand workspace.

```
GET https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-entity-counts-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wisewand `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-entity-counts-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-entity-counts-summary?${params}`, {
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
| `projectId` | string | no | Wisewand query parameter `projectId`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "articles": 1,
      "categorypages": 1,
      "discoverarticles": 1,
      "productpages": 1,
      "rssfeedtriggers": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `articles` | number |  |
| `categorypages` | number |  |
| `discoverarticles` | number |  |
| `productpages` | number |  |
| `rssfeedtriggers` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Wisewand API, this operation is `GET /v1/entities/summary/` (base URL `https://api.wisewand.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-entity-counts-summary.md) for the provider-specific parameters and requirements.

