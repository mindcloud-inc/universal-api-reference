# Strategypoint: List Attachments

Retrieves attachments from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-attachments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-attachments?${params}`, {
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
| `count` | number | no | Maximum number of attachments to return. |
| `object` | string | no | Filter attachments by related object type. |
| `objectId` | number | no | Filter attachments by related object identifier. |
| `search` | string | no | Search text to match attachment names or metadata. |
| `start` | number | no | Offset into the attachment result set. |

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
      "name": "Ava Chen",
      "object": "string",
      "objectId": 1,
      "uploadDate": "string"
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
| `name` | string | The attachment name. |
| `object` | string | The related object type. |
| `objectId` | number | The related object identifier. |
| `uploadDate` | string | The upload timestamp. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /attachments` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-attachments.md) for the provider-specific parameters and requirements.

