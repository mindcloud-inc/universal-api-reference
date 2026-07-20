# TextingHouse: Get SMS Status By Client Message ID

Retrieves TextingHouse SMS status by client message ID.

```
GET https://connect.mindcloud.co/v1/universal/textingHouse/latest/actions/get-sms-status-by-client-message-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TextingHouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/textingHouse/latest/actions/get-sms-status-by-client-message-id?connectionId=$CONNECTION_ID&climsgid=FRS78913246" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "climsgid": "FRS78913246"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/textingHouse/latest/actions/get-sms-status-by-client-message-id?${params}`, {
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
| `climsgid` | string | yes | Client-defined message identifier used for later status lookups. Example: `FRS78913246`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rawResponse": "string",
      "statusCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rawResponse` | string | Plain-text response returned by TextingHouse. |
| `statusCode` | string | Current TextingHouse status code for the requested message. |

## Native endpoint

Through the native TextingHouse API, this operation is `POST /do` (base URL `https://api.textinghouse.com/http/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sms-status-by-client-message-id.md) for the provider-specific parameters and requirements.

