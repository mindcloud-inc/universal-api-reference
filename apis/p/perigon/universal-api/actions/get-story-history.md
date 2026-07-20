# Perigon: Get Story History

Retrieves historical changes for Perigon stories over time.

```
GET https://connect.mindcloud.co/v1/universal/perigon/latest/actions/get-story-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perigon `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perigon/latest/actions/get-story-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/perigon/latest/actions/get-story-history?${params}`, {
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
| `clusterId` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `cluster_123`. |
| `from` | date | no | Example: `2026-04-01T00:00:00`. |
| `to` | date | no | Example: `2026-04-09T23:59:59`. |
| `sortBy` | string | no | Example: `createdAt`. |
| `page` | number | no | Example: `0`. |
| `size` | number | no | Example: `10`. |
| `changelogExists` | boolean | no |  |

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

Through the native Perigon API, this operation is `GET /v1/stories/history` (base URL `https://api.perigon.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-story-history.md) for the provider-specific parameters and requirements.

