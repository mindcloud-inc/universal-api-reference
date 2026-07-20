# SendX: Get Template



```
GET https://connect.mindcloud.co/v1/universal/sendX/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendX/latest/actions/get-template?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendX/latest/actions/get-template?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | no | The SendX template identifier. |

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

Through the native SendX API, this operation is `GET /template/email/:identifier` (base URL `https://api.sendx.io/api/v1/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

