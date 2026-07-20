# Zoho Sheet: Copy Workbook

Creates a copy of a workbook in Zoho Sheet.

```
POST https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/copy-workbook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/copy-workbook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/copy-workbook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceId` | string | yes | The resource id of the workbook that needs to be copied |
| `workbookName` | string | no | Optional parameter. Name of the copied workbook |
| `parentId` | string | no | Optional parameter. The unique ID of the destination folder. By default My Folder of Zoho Workdrive is the destination folder. |
| `copyLockSettings` | boolean | no | Optional parameter. Default value is true. If set to false the range/worksheet lock settings from the parent document will not be copied. |

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
      "workbookUrl": "https://example.com"
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

## Native endpoint

Through the native Zoho Sheet API, this operation is `POST /copy` (base URL `https://sheet.zoho.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-workbook.md) for the provider-specific parameters and requirements.

