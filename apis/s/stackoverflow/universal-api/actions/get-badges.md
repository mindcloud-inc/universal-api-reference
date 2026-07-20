# Stackoverflow: Get Badges

Retrieves specific badges from Stackoverflow.

```
GET https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/get-badges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackoverflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/get-badges?connectionId=$CONNECTION_ID&limit=25&offset=0&ids=string&site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "ids": "string",
  "site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/get-badges?${params}`, {
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
| `ids` | string | yes | Semicolon-separated Stack Exchange badge IDs. |
| `site` | string | yes | Stack Exchange site parameter, for example stackoverflow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "award_count": 1,
      "badge_id": 1,
      "badge_type": "string",
      "link": "https://example.com",
      "name": "Ava Chen",
      "rank": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `award_count` | number |  |
| `badge_id` | number |  |
| `badge_type` | string |  |
| `link` | string |  |
| `name` | string |  |
| `rank` | string |  |

## Native endpoint

Through the native Stackoverflow API, this operation is `GET /badges/[:ids]` (base URL `https://api.stackexchange.com/2.3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-badges.md) for the provider-specific parameters and requirements.

