# Xola: Create Event

Creates a new event in Xola.

```
POST https://connect.mindcloud.co/v1/universal/xola/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xola `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xola/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "experience.id": "string",
  "start": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xola/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "experience.id": "string",
    "start": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `experience.id` | string | yes |  |
| `start` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "experience": {
        "id": "string"
      },
      "id": "string",
      "object": "string",
      "seller": {
        "id": "string"
      },
      "start": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `experience.id` | string | Associated experience identifier. |
| `id` | string | Event identifier. |
| `object` | string | Xola object type. |
| `seller.id` | string | Owning seller identifier. |
| `start` | date | Event start time. |

## Native endpoint

Through the native Xola API, this operation is `POST /events` (base URL `https://sandbox.xola.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

