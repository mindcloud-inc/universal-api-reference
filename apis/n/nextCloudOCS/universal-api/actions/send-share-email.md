# Next Cloud OCS: Send Share Email

Sends a share email in Next Cloud OCS.

```
POST https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/send-share-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Next Cloud OCS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/send-share-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shareId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/send-share-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shareId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shareId` | string | yes | Numeric share ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "status": "string",
      "statuscode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `message` | string |  |
| `status` | string |  |
| `statuscode` | number |  |

## Native endpoint

Through the native Next Cloud OCS API, this operation is `POST /ocs/v2.php/apps/files_sharing/api/v1/shares/{{shareId}}/send-email` (base URL `https://demo2.nextcloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-share-email.md) for the provider-specific parameters and requirements.

