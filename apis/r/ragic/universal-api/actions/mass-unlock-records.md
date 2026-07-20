# Ragic: Mass Unlock Records

Unlocks multiple records in Ragic.

```
PUT https://connect.mindcloud.co/v1/universal/ragic/latest/actions/mass-unlock-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ragic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ragic/latest/actions/mass-unlock-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tabFolderPath": "string",
  "sheetIndex": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ragic/latest/actions/mass-unlock-records', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tabFolderPath": "string",
    "sheetIndex": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tabFolderPath` | string | yes | Folder path segment before the sheet index in the Ragic URL, for example ragic-setup. |
| `sheetIndex` | number | yes | Numeric sheet identifier from the target Ragic resource URL. |
| `recordId` | number | no | Single Ragic record ID to target for the mass operation when you are not using a where filter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `where` | string | no | Optional Ragic where clause in the documented `<fieldId>,<operand>,<value>` format for targeting multiple records. Example: `1,eq,apps@mindcloud.co`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `taskId` | string | UUID for tracking the asynchronous Ragic mass operation. |

## Native endpoint

Through the native Ragic API, this operation is `POST /:tabFolderPath/:sheetIndex/massOperation/massLock` (base URL `{{credentials.serverUrl}}/mindcloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mass-unlock-records.md) for the provider-specific parameters and requirements.

