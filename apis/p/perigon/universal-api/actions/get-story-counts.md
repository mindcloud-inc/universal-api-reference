# Perigon: Get Story Counts

Retrieves Perigon story counts grouped by filters or dimensions.

```
GET https://connect.mindcloud.co/v1/universal/perigon/latest/actions/get-story-counts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perigon `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perigon/latest/actions/get-story-counts?connectionId=$CONNECTION_ID&limit=25&offset=0&splitBy=DAY" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "splitBy": "DAY"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/perigon/latest/actions/get-story-counts?${params}`, {
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
| `splitBy` | string | yes | Example: `DAY`. |
| `q` | string | no | Example: `inflation`. |
| `page` | number | no | Example: `0`. |
| `size` | number | no | Example: `10`. |
| `from` | date | no | Example: `2026-04-01T00:00:00`. |
| `to` | date | no | Example: `2026-04-09T23:59:59`. |
| `topic` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `Markets`. |
| `category` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `Finance`. |
| `source` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `wsj.com`. |
| `country` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `us`. |
| `personName` | string | no | Example: `Donald Trump`. |
| `companyName` | string | no | Example: `NVIDIA`. |
| `showNumResults` | boolean | no |  |
| `expandArticles` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {}
      ],
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> |  |
| `status` | number |  |

## Native endpoint

Through the native Perigon API, this operation is `GET /v1/stories/stats` (base URL `https://api.perigon.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-story-counts.md) for the provider-specific parameters and requirements.

