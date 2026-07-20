# Viesus: Complete Signed Upload

Completes a signed upload in Viesus.

```
PUT https://connect.mindcloud.co/v1/universal/viesus/latest/actions/complete-signed-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viesus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/viesus/latest/actions/complete-signed-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viesus/latest/actions/complete-signed-upload', {
  method: 'PUT',
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
      "completeSignedUpload": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completeSignedUpload` | object | Completed signed upload. |

## Native endpoint

Through the native Viesus API, this operation is `POST /` (base URL `https://api.viesus.cloud/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-signed-upload.md) for the provider-specific parameters and requirements.

