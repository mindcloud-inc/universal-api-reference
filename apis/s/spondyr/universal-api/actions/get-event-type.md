# Spondyr: Get Event Type

Retrieves an event type for a transaction type in Spondyr.

```
GET https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/get-event-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spondyr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/get-event-type?connectionId=$CONNECTION_ID&eventType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/get-event-type?${params}`, {
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
| `eventType` | string | yes | The event type name to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "APIStatus": "string",
      "ErrorMessage": "string",
      "Name": "Ava Chen",
      "TransactionType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `APIStatus` | string |  |
| `ErrorMessage` | string |  |
| `Name` | string |  |
| `TransactionType` | string |  |

## Native endpoint

Through the native Spondyr API, this operation is `GET /EventType` (base URL `https://client.spondyr.io/api/v1.0.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-type.md) for the provider-specific parameters and requirements.

