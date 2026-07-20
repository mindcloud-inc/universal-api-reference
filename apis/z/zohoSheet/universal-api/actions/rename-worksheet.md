# Zoho Sheet: Rename Worksheet

Renames an existing worksheet in Zoho Sheet.

```
PUT https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/rename-worksheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/rename-worksheet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceId": "string",
  "oldName": "Ava Chen",
  "newName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/rename-worksheet', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceId": "string",
    "oldName": "Ava Chen",
    "newName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceId` | string | yes | The workbook resource ID. |
| `oldName` | string | yes | Name of the existing worksheet |
| `newName` | string | yes | New name that needs to be set |

## Response

```json
{
  "success": true,
  "data": [
    {
      "method": "string",
      "status": "string",
      "worksheetNames": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `method` | string |  |
| `status` | string |  |
| `worksheetNames[]` | array<object> |  |
| `worksheetNames[].worksheetId` | string |  |
| `worksheetNames[].worksheetName` | string |  |

## Native endpoint

Through the native Zoho Sheet API, this operation is `POST /:resourceId` (base URL `https://sheet.zoho.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-worksheet.md) for the provider-specific parameters and requirements.

