# EMnify: List Events

Retrieves a list of events from EMnify.

```
GET https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0&authToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "authToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-events?${params}`, {
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
| `authToken` | string | yes | Auth token from Retrieve Authentication Token. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `q` | string | no | Optional event filter in <filter>:<value> format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alert": true,
      "customEventId": {},
      "description": "string",
      "detail": {
        "country": {
          "id": 1,
          "isoCode": "string",
          "name": "Ava Chen"
        },
        "invoiceIssuer": {
          "description": "string",
          "id": 1
        }
      },
      "eventSeverity": {
        "description": "string",
        "id": 1
      },
      "eventSource": {
        "description": "string",
        "id": 1
      },
      "eventType": {
        "description": "string",
        "id": 1
      },
      "id": 1,
      "organisation": {
        "id": 1,
        "name": "Ava Chen"
      },
      "timestamp": "2026-05-07T12:00:00.000Z",
      "user": {
        "id": 1,
        "name": "Ava Chen",
        "username": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alert` | boolean |  |
| `customEventId` | object |  |
| `description` | string |  |
| `detail.country.id` | number |  |
| `detail.country.isoCode` | string |  |
| `detail.country.name` | string |  |
| `detail.invoiceIssuer.description` | string |  |
| `detail.invoiceIssuer.id` | number |  |
| `eventSeverity.description` | string |  |
| `eventSeverity.id` | number |  |
| `eventSource.description` | string |  |
| `eventSource.id` | number |  |
| `eventType.description` | string |  |
| `eventType.id` | number |  |
| `id` | number |  |
| `organisation.id` | number |  |
| `organisation.name` | string |  |
| `timestamp` | date |  |
| `user.id` | number |  |
| `user.name` | string |  |
| `user.username` | string |  |

## Native endpoint

Through the native EMnify API, this operation is `GET /event` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

