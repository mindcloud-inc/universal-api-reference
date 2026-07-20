# Flatfile: Insert Records

Creates new records in a Flatfile sheet.

```
POST https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/insert-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flatfile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/insert-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sheetId": "us_sht_mindcloud_flatfile"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/insert-records', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sheetId": "us_sht_mindcloud_flatfile"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sheetId` | string | yes | Flatfile sheet ID. Default: `us_sht_mindcloud_flatfile`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Inserted record result. |

## Native endpoint

Through the native Flatfile API, this operation is `POST /sheets/:sheetId/records` (base URL `https://api.x.flatfile.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-records.md) for the provider-specific parameters and requirements.

