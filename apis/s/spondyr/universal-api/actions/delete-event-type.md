# Spondyr: Delete Event Type

Deletes an existing event type for a transaction type from Spondyr.

```
DELETE https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/delete-event-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spondyr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/delete-event-type?connectionId=$CONNECTION_ID&eventType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/delete-event-type?${params}`, {
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
| `eventType` | string | yes | The event type name to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "APIStatus": "string",
      "ErrorMessage": "string"
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

## Native endpoint

Through the native Spondyr API, this operation is `DELETE /EventType` (base URL `https://client.spondyr.io/api/v1.0.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-event-type.md) for the provider-specific parameters and requirements.

