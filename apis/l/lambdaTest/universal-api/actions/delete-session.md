# LambdaTest: Delete Session

Deletes an existing session from LambdaTest.

```
DELETE https://connect.mindcloud.co/v1/universal/lambdaTest/latest/actions/delete-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LambdaTest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/lambdaTest/latest/actions/delete-session?connectionId=$CONNECTION_ID&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lambdaTest/latest/actions/delete-session?${params}`, {
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
| `sessionId` | string | yes | The LambdaTest session ID. |

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

Through the native LambdaTest API, this operation is `DELETE /sessions/{session_id}` (base URL `https://api.lambdatest.com/automation/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-session.md) for the provider-specific parameters and requirements.

