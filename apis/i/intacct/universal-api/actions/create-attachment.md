# Sage Intacct: Create Attachment

Create a supporting document in a Sage Intacct attachment folder, with optional files encoded as base64.

```
POST https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sage Intacct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-attachment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "attachments[].attachmentdata": "string",
  "attachments[].attachmenttype": "string",
  "supdocname": "Ava Chen",
  "attachments[].attachmentname": "Ava Chen",
  "supdocfoldername": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-attachment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "attachments[].attachmentdata": "string",
    "attachments[].attachmenttype": "string",
    "supdocname": "Ava Chen",
    "attachments[].attachmentname": "Ava Chen",
    "supdocfoldername": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachments[].attachmentdata` | string | yes | Base64-encoded binary file content. |
| `supdocid` | string | no | Required only when attachment autonumbering is not configured in Sage Intacct. |
| `attachments[].attachmenttype` | string | yes | File extension without a period, for example pdf. |
| `supdocname` | string<object> | yes |  |
| `attachments[].attachmentname` | string<object> | yes | File name without the period or extension. |
| `supdocfoldername` | string | yes |  |
| `supdocdescription` | string | no |  |
| `locationid` | string | no | Optional entity location ID for a multi-entity Sage Intacct login. |
| `attachments[]` | array<object> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sage Intacct API returns.

## Native endpoint

Through the native Sage Intacct API, this operation is `POST` (base URL `https://api.intacct.com/ia/xml/xmlgw.phtml`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-attachment.md) for the provider-specific parameters and requirements.

