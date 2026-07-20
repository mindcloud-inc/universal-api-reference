# Flatfile: Bulk Update Records

Bulk updates matching records in a Flatfile sheet.

```
PUT https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/bulk-update-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flatfile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/bulk-update-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fieldUpdates": [
    {
      "value": "processed",
      "fieldKey": "status"
    }
  ],
  "sheetId": "us_sht_mindcloud_flatfile"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/bulk-update-records', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fieldUpdates": [{"value":"processed","fieldKey":"status"}],
    "sheetId": "us_sht_mindcloud_flatfile"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fieldUpdates` | string | yes | Field updates payload. Default: `[{"value":"processed","fieldKey":"status"}]`. |
| `sheetId` | string | yes | Flatfile sheet identifier. Default: `us_sht_mindcloud_flatfile`. |

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
| `data` | object | Bulk update result. |

## Native endpoint

Through the native Flatfile API, this operation is `PATCH /sheets/:sheetId/records/bulk-update` (base URL `https://api.x.flatfile.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-records.md) for the provider-specific parameters and requirements.

