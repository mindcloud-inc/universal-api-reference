# Strategypoint: Get Attachment

Retrieves an attachment from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-attachment?connectionId=$CONNECTION_ID&attachmentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "attachmentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-attachment?${params}`, {
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
| `attachmentId` | number | yes | The unique attachment identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachmentId": 1,
      "fileExists": true,
      "filename": "Ava Chen",
      "filetype": "string",
      "link": {},
      "name": "Ava Chen",
      "object": "string",
      "objectId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachmentId` | number | The unique attachment identifier. |
| `fileExists` | boolean | Whether the backing file is available. |
| `filename` | string | The uploaded file name. |
| `filetype` | string | The attachment file type. |
| `link` | object | Link metadata for the attachment. |
| `name` | string | The attachment name. |
| `object` | string | The related object type. |
| `objectId` | number | The related object identifier. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /attachments/{attachmentId}` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attachment.md) for the provider-specific parameters and requirements.

