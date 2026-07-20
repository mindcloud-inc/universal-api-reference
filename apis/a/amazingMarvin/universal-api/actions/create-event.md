# Amazing Marvin: Create Event

Creates an event in Amazing Marvin.

```
POST https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazing Marvin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "start": "string",
  "length": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "start": "string",
    "length": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Event title. |
| `start` | string | yes | ISO formatted start time. |
| `length` | number | yes | Event length in milliseconds. |
| `note` | string | no | Optional event note in markdown. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "db": "string",
      "length": 1,
      "note": "string",
      "start": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `db` | string |  |
| `length` | number |  |
| `note` | string |  |
| `start` | date |  |
| `title` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Amazing Marvin API, this operation is `POST /addEvent` (base URL `https://serv.amazingmarvin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

