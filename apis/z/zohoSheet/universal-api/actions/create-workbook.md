# Zoho Sheet: Create Workbook

Creates a new workbook in Zoho Sheet.

```
POST https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/create-workbook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/create-workbook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workbookName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/create-workbook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workbookName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workbookName` | string | yes | Name of the new workbook |
| `parentId` | string | no | Optional parameter. The unique ID of the destination folder. By default My Folder of Zoho Workdrive is the destination folder. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "method": "string",
      "resourceId": "string",
      "status": "string",
      "workbookName": "Ava Chen",
      "workbookUrl": "https://example.com",
      "worksheetId": "string",
      "worksheetName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `method` | string |  |
| `resourceId` | string |  |
| `status` | string |  |
| `workbookName` | string |  |
| `workbookUrl` | string |  |
| `worksheetId` | string |  |
| `worksheetName` | string |  |

## Native endpoint

Through the native Zoho Sheet API, this operation is `POST /create` (base URL `https://sheet.zoho.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workbook.md) for the provider-specific parameters and requirements.

