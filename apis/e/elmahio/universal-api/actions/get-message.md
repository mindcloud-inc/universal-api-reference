# elmah.io: Get Message

Retrieves a message from elmah.io.

```
GET https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a elmah.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/get-message?connectionId=$CONNECTION_ID&id=string&logId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "logId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/get-message?${params}`, {
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
| `id` | string | yes | The ID of the message to fetch. |
| `logId` | string | yes | The ID of the log containing the message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateTime": "string",
      "detail": "string",
      "id": "string",
      "severity": "string",
      "statusCode": 1,
      "title": "string",
      "titleTemplate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateTime` | string |  |
| `detail` | string |  |
| `id` | string |  |
| `severity` | string |  |
| `statusCode` | number |  |
| `title` | string |  |
| `titleTemplate` | string |  |

## Native endpoint

Through the native elmah.io API, this operation is `GET /v3/messages/:logId/:id` (base URL `https://api.elmah.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

