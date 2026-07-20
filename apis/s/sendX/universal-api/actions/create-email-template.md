# SendX: Create Email Template



```
POST https://connect.mindcloud.co/v1/universal/sendX/latest/actions/create-email-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendX/latest/actions/create-email-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "subject": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendX/latest/actions/create-email-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "subject": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `subject` | string | yes |  |
| `htmlCode` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateCode` | string | no |  |
| `editorType` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "editorType": 1,
      "htmlCode": "string",
      "id": "string",
      "name": "Ava Chen",
      "previewText": "string",
      "templateCode": "string",
      "thumbnail": "string",
      "type": 1,
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `editorType` | number |  |
| `htmlCode` | string |  |
| `id` | string |  |
| `name` | string |  |
| `previewText` | string |  |
| `templateCode` | string |  |
| `thumbnail` | string |  |
| `type` | number |  |
| `updated` | date |  |

## Native endpoint

Through the native SendX API, this operation is `POST /template/email` (base URL `https://api.sendx.io/api/v1/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-email-template.md) for the provider-specific parameters and requirements.

