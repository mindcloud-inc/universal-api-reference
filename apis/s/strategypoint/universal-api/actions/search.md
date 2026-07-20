# Strategypoint: Search

Finds matching elements in Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/search?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/search?${params}`, {
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
| `count` | number | no | Maximum number of results to return. |
| `object` | string | no | Limit search to a related object type. |
| `page` | number | no | Page number to return. |
| `periodId` | number | no | Limit search to a period. |
| `scorecardId` | number | no | Limit search to a scorecard. |
| `type` | string | no | Limit search to a specific result type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "object": "string",
      "objectId": 1,
      "pageCount": 1,
      "parameters": {},
      "results": [
        {}
      ],
      "scorecardId": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | The matched object name. |
| `object` | string | The matched object type. |
| `objectId` | number | The matched object identifier. |
| `pageCount` | number | The number of pages in the search result set. |
| `parameters` | object | The effective search parameters. |
| `results` | array<object> | The matched search results. |
| `scorecardId` | number | The related scorecard identifier. |
| `totalCount` | number | The total number of matched results. |

## Native endpoint

Through the native Strategypoint API, this operation is `POST /search` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search.md) for the provider-specific parameters and requirements.

