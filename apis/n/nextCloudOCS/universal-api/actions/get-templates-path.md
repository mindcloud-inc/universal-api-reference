# Next Cloud OCS: Get Templates Path

Retrieves templates path from Next Cloud OCS.

```
POST https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/get-templates-path
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Next Cloud OCS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/get-templates-path" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/get-templates-path', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "ocs": {},
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
| `data` | object | Primary response payload returned by the endpoint. |
| `message` | string | Human-readable status or error message when provided. |
| `ocs` | object | OCS metadata wrapper returned by Nextcloud. |
| `status` | string | Endpoint status value when provided. |
| `statuscode` | number | Nextcloud OCS status code when provided. |

## Native endpoint

Through the native Next Cloud OCS API, this operation is `POST /ocs/v2.php/apps/files/api/v1/templates/path` (base URL `https://demo2.nextcloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-templates-path.md) for the provider-specific parameters and requirements.

