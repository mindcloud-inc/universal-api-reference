# Zoho ZeptoMail: Create Export

Creates a new export for Zoho ZeptoMail logs.

```
POST https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/create-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho ZeptoMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/create-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "exportType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/create-export', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "exportType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bcc` | string | no | BCC recipient filter for exports. |
| `bounceCategory` | string | no | Bounce category filter for mail-log exports. |
| `cc` | string | no | CC recipient filter for exports. |
| `clientReference` | string | no | Client reference filter for exports. |
| `dateFrom` | string | no | Start date for the export window. |
| `dateTo` | string | no | End date for the export window. |
| `dndType` | string | no | Suppression export type: email or domain. |
| `entity` | string | no | Activity-log entity to export. |
| `exportType` | string | yes | Export category to create. |
| `from` | string | no | Sender address to filter exports by. |
| `isDelivered` | boolean | no | Include delivered email logs in the export. |
| `isHb` | boolean | no | Include hard bounce logs in the export. |
| `isMailfailure` | boolean | no | Include processed failed email logs in the export. |
| `isSb` | boolean | no | Include soft bounce logs in the export. |
| `mailAgentKey` | string | no | Agent alias to export logs for. |
| `modifiedBy` | string | no | User who modified the exported activity entity. |
| `password` | string | no | Optional password to protect the exported file. |
| `subject` | string | no | Email subject filter for exports. |
| `to` | string | no | Recipient address to filter exports by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "created_time": "2026-05-07T12:00:00.000Z",
        "export_id": "string",
        "export_type": "string",
        "modified_time": "2026-05-07T12:00:00.000Z",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.created_time` | date |  |
| `data.export_id` | string |  |
| `data.export_type` | string |  |
| `data.modified_time` | date |  |
| `data.status` | string |  |

## Native endpoint

Through the native Zoho ZeptoMail API, this operation is `POST :exportType/exports` (base URL `https://api.zeptomail.com/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-export.md) for the provider-specific parameters and requirements.

