# UbiBot: Import Feeds From CSV

Imports channel feeds from a CSV file in UbiBot.

```
POST https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/import-feeds-from-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UbiBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/import-feeds-from-csv" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/import-feeds-from-csv', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "desp": "string",
      "errorCode": "string",
      "result": "string",
      "server_time": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `desp` | string | UbiBot error description when the import request fails. |
| `errorCode` | string | UbiBot error code when the import request fails. |
| `result` | string | UbiBot success or error result status. |
| `server_time` | date | UbiBot server timestamp. |

## Native endpoint

Through the native UbiBot API, this operation is `POST /update.csv` (base URL `https://webapi.ubibot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-feeds-from-csv.md) for the provider-specific parameters and requirements.

