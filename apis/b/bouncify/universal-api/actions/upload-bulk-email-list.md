# Bouncify: Upload Bulk Email List

Uploads a bulk email list to Bouncify.

```
POST https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/upload-bulk-email-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bouncify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/upload-bulk-email-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/upload-bulk-email-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `autoVerify` | string | no | Set true to upload the list and immediately start verification. Default: `false`. |
| `emails` | object | yes | Array of email objects to upload for bulk verification. Accepts multiple values as an array. |
| `title` | string | no | Friendly name for the bulk verification list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string | Bulk verification job identifier. |
| `message` | string | Provider message describing the upload result. |
| `success` | boolean | Whether the bulk upload request succeeded. |

## Native endpoint

Through the native Bouncify API, this operation is `POST /bulk` (base URL `https://api.bouncify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-bulk-email-list.md) for the provider-specific parameters and requirements.

