# Reamaze: Create Incident



```
POST https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/create-incident
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reamaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/create-incident" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "incident": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/create-incident', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "incident": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `incident` | object | yes | Body payload field documented on https://www.reamaze.com/api/post_incident. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "incidentsSystems": [
        {}
      ],
      "status": "string",
      "title": "string",
      "updatedAt": "string",
      "updates": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `incidentsSystems` | array<object> |  |
| `status` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `updates` | array<object> |  |

## Native endpoint

Through the native Reamaze API, this operation is `POST /incidents` (base URL `https://{{credentials.brand}}.reamaze.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-incident.md) for the provider-specific parameters and requirements.

