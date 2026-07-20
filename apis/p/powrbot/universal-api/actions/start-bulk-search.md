# Powrbot: Start Bulk Search

Creates a bulk search job in Powrbot.

```
POST https://connect.mindcloud.co/v1/universal/powrbot/latest/actions/start-bulk-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Powrbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/powrbot/latest/actions/start-bulk-search" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "csv_file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/powrbot/latest/actions/start-bulk-search', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "csv_file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `csv_file` | file | yes | CSV file containing company names, one per row. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_count": 1,
      "count": 1,
      "count_completed": 1,
      "id": 1,
      "is_completed": true,
      "search_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_count` | number |  |
| `count` | number |  |
| `count_completed` | number |  |
| `id` | number |  |
| `is_completed` | boolean |  |
| `search_type` | string |  |

## Native endpoint

Through the native Powrbot API, this operation is `POST /search/` (base URL `https://powrbot.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-bulk-search.md) for the provider-specific parameters and requirements.

