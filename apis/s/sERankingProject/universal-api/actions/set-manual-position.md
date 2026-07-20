# SE Ranking Project: Set Manual Position

Updates a keyword's ranking position in SE Ranking.

```
PUT https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/set-manual-position
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/set-manual-position" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "date": "string",
  "keyword_id": 1,
  "position": 1,
  "site_engine_id": 1,
  "site_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/set-manual-position', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "date": "string",
    "keyword_id": 1,
    "position": 1,
    "site_engine_id": 1,
    "site_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date` | string | yes |  |
| `keyword_id` | number | yes |  |
| `position` | number | yes |  |
| `site_engine_id` | number | yes |  |
| `site_id` | list<number> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | array | The raw response body. The saved successful response was an empty array (HTTP 200). |

## Native endpoint

Through the native SE Ranking Project API, this operation is `PUT /sites/:site_id/position` (base URL `https://api4.seranking.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-manual-position.md) for the provider-specific parameters and requirements.

