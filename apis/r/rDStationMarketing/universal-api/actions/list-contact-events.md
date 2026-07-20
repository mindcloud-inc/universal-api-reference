# RD Station Marketing: List Contact Events



```
GET https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-contact-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station Marketing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-contact-events?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-contact-events?${params}`, {
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
| `uuid` | string | yes | Contact UUID in path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "eventFamily": "string",
      "eventIdentifier": "string",
      "eventTimestamp": "2026-05-07T12:00:00.000Z",
      "eventType": "string",
      "payload": {
        "email": "ava@example.com",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `eventFamily` | string |  |
| `eventIdentifier` | string |  |
| `eventTimestamp` | date |  |
| `eventType` | string |  |
| `payload.email` | string |  |
| `payload.name` | string |  |

## Native endpoint

Through the native RD Station Marketing API, this operation is `GET /platform/contacts/:uuid/events` (base URL `https://api.rd.services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-events.md) for the provider-specific parameters and requirements.

