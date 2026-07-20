# YepCode: Execute process async

Creates an asynchronous process execution in YepCode.

```
POST https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/execute-process-async
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YepCode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/execute-process-async" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string",
  "parameters": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/execute-process-async', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string",
    "parameters": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | yes |  |
| `parameters` | string | yes |  |
| `comment` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "executionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `executionId` | string |  |

## Native endpoint

Through the native YepCode API, this operation is `POST /processes/:identifier/execute` (base URL `https://cloud.yepcode.io/api/{{credentials.team}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-process-async.md) for the provider-specific parameters and requirements.

