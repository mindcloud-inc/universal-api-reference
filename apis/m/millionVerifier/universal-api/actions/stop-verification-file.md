# MillionVerifier: Stop Verification File

Stops a verification file in MillionVerifier.

```
PUT https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/stop-verification-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MillionVerifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/stop-verification-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/stop-verification-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileId` | number | yes | The ID of the uploaded file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |

## Native endpoint

Through the native MillionVerifier API, this operation is `GET https://bulkapi.millionverifier.com/bulkapi/stop` (base URL `https://api.millionverifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stop-verification-file.md) for the provider-specific parameters and requirements.

