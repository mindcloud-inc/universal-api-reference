# Postman: List Mock Server Call Logs

Retrieves call logs for a mock server in Postman.

```
GET https://connect.mindcloud.co/v1/universal/postman/latest/actions/list-mock-server-call-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postman/latest/actions/list-mock-server-call-logs?connectionId=$CONNECTION_ID&mockId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mockId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postman/latest/actions/list-mock-server-call-logs?${params}`, {
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
| `mockId` | string | yes | The mock server's ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "nextCursor": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta.nextCursor` | string |  |

## Native endpoint

Through the native Postman API, this operation is `GET /mocks/:mockId/call-logs` (base URL `https://api.getpostman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mock-server-call-logs.md) for the provider-specific parameters and requirements.

