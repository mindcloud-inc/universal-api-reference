# LambdaTest: Upload User File

Uploads a user file to LambdaTest.

```
POST https://connect.mindcloud.co/v1/universal/lambdaTest/latest/actions/upload-user-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LambdaTest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lambdaTest/latest/actions/upload-user-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lambdaTest/latest/actions/upload-user-file', {
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
      "status": "string"
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

## Native endpoint

Through the native LambdaTest API, this operation is `POST /user-files` (base URL `https://api.lambdatest.com/automation/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-user-file.md) for the provider-specific parameters and requirements.

