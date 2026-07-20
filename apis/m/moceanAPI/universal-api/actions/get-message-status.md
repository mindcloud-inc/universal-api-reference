# Mocean API: Get Message Status



```
GET https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/get-message-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mocean API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/get-message-status?connectionId=$CONNECTION_ID&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/get-message-status?${params}`, {
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
| `messageId` | string | yes | The Mocean message ID to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditDeducted": "string",
      "errMsg": "string",
      "messageStatus": 1,
      "msgid": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditDeducted` | string |  |
| `errMsg` | string |  |
| `messageStatus` | number |  |
| `msgid` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Mocean API API, this operation is `GET /rest/2/report/message?mocean-resp-format=json` (base URL `https://rest.moceanapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message-status.md) for the provider-specific parameters and requirements.

