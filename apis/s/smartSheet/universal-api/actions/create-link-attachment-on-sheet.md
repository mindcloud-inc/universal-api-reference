# Smartsheet: Create Link Attachment on Sheet

Creates a link attachment on a Smartsheet sheet.

```
POST https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/create-link-attachment-on-sheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartsheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/create-link-attachment-on-sheet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sheetId": 1,
  "name": "Ava Chen",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/create-link-attachment-on-sheet', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sheetId": 1,
    "name": "Ava Chen",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sheetId` | number | yes |  |
| `name` | string | yes |  |
| `url` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no |  |
| `attachmentSubType` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "result": {
        "attachmentType": "string",
        "createdAt": "string",
        "createdBy": {
          "email": "ava@example.com",
          "name": "Ava Chen"
        },
        "id": 1,
        "name": "Ava Chen",
        "parentId": 1,
        "parentType": "string",
        "url": "https://example.com"
      },
      "resultCode": 1,
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `result.attachmentType` | string |  |
| `result.createdAt` | string |  |
| `result.createdBy.email` | string |  |
| `result.createdBy.name` | string |  |
| `result.id` | number |  |
| `result.name` | string |  |
| `result.parentId` | number |  |
| `result.parentType` | string |  |
| `result.url` | string |  |
| `resultCode` | number |  |
| `version` | number |  |

## Native endpoint

Through the native Smartsheet API, this operation is `POST /sheets/:sheetId/attachments` (base URL `https://api.smartsheet.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-link-attachment-on-sheet.md) for the provider-specific parameters and requirements.

