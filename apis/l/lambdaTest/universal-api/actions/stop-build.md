# LambdaTest: Stop Build

Stops a build in LambdaTest.

```
PUT https://connect.mindcloud.co/v1/universal/lambdaTest/latest/actions/stop-build
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LambdaTest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lambdaTest/latest/actions/stop-build" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "buildId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lambdaTest/latest/actions/stop-build', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "buildId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `buildId` | string | yes | The LambdaTest build ID to stop. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "Meta": {},
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
| `Meta` | object |  |
| `status` | string |  |

## Native endpoint

Through the native LambdaTest API, this operation is `PUT /build/stop` (base URL `https://api.lambdatest.com/automation/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stop-build.md) for the provider-specific parameters and requirements.

