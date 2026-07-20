# Podio: Attach File

Attaches a file to a Podio object.

```
POST https://connect.mindcloud.co/v1/universal/podio/latest/actions/attach-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/podio/latest/actions/attach-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "12345",
  "refType": "item",
  "refId": "987654"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/podio/latest/actions/attach-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "12345",
    "refType": "item",
    "refId": "987654"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileId` | string | yes | The ID of the uploaded file to attach. Example: `12345`. |
| `refType` | string | yes | The type of object the file should be attached to. Example: `item`. |
| `refId` | number | yes | The ID of the object the file should be attached to. Example: `987654`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `silent` | boolean | no | Suppress stream bumping and notifications for the attachment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Empty response body on success. |

## Native endpoint

Through the native Podio API, this operation is `POST /file/:file_id/attach` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/attach-file.md) for the provider-specific parameters and requirements.

