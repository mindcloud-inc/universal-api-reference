# Firecrawl: Execute Browser Code

Executes code in a Firecrawl browser session.

```
PUT https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/execute-browser-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firecrawl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/execute-browser-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "string",
  "code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/execute-browser-code', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "string",
    "code": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionId` | string | yes | The browser session ID |
| `code` | string | yes | Code to execute in the browser sandbox |
| `language` | string | no | Language of the code to execute |
| `timeout` | number | no | Execution timeout in seconds |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exitCode": 1,
      "killed": true,
      "result": "string",
      "stderr": "string",
      "stdout": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exitCode` | number |  |
| `killed` | boolean |  |
| `result` | string |  |
| `stderr` | string |  |
| `stdout` | string |  |

## Native endpoint

Through the native Firecrawl API, this operation is `POST /browser/:sessionId/execute` (base URL `https://api.firecrawl.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-browser-code.md) for the provider-specific parameters and requirements.

