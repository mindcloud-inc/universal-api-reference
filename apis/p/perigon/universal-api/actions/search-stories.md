# Perigon: Search Stories

Finds clustered news stories in Perigon by keywords and filters.

```
GET https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-stories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perigon `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-stories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-stories?${params}`, {
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
| `q` | string | no | Example: `climate change`. |
| `clusterId` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `cluster_123`. |
| `sortBy` | string | no | Example: `updatedAt`. |
| `page` | number | no | Example: `0`. |
| `size` | number | no | Example: `10`. |
| `from` | date | no | Example: `2026-04-01T00:00:00`. |
| `to` | date | no | Example: `2026-04-09T23:59:59`. |
| `updatedFrom` | date | no | Example: `2026-04-01T00:00:00`. |
| `updatedTo` | date | no | Example: `2026-04-09T23:59:59`. |
| `topic` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `Markets`. |
| `category` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `Business`. |
| `source` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `cnn.com`. |
| `country` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `us`. |
| `personName` | string | no | Example: `Jerome Powell`. |
| `companyName` | string | no | Example: `Tesla`. |
| `showNumResults` | boolean | no |  |
| `expandArticles` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "numResults": 1,
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
| `numResults` | number |  |
| `results` | array<object> |  |
| `status` | number |  |

## Native endpoint

Through the native Perigon API, this operation is `GET /v1/stories/all` (base URL `https://api.perigon.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-stories.md) for the provider-specific parameters and requirements.

