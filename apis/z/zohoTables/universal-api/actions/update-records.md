# Zoho Tables: Update Records

Updates records in Zoho Tables by criteria or record IDs.

```
PUT https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/update-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Tables `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/update-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "baseId": "string",
  "tableId": "string",
  "data": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/update-records', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "baseId": "string",
    "tableId": "string",
    "data": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `baseId` | string | yes |  |
| `tableId` | string | yes |  |
| `viewId` | string | no |  |
| `data` | string | yes |  |
| `isIdsUsedInData` | boolean | no |  |
| `criteria` | string | no |  |
| `isIdsUsedInParams` | boolean | no |  |
| `firstMatchOnly` | boolean | no |  |
| `isCaseSensitive` | boolean | no |  |
| `isUpsertNeeded` | boolean | no |  |
| `recordIds` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "displayData": {},
      "recordId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Record values keyed by field ID. |
| `displayData` | object | Display-friendly record values keyed by field ID. |
| `recordId` | string | Zoho record identifier. |

## Native endpoint

Through the native Zoho Tables API, this operation is `PUT /records` (base URL `https://tables.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-records.md) for the provider-specific parameters and requirements.

