# Reamaze: Update Incident



```
PUT https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/update-incident
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reamaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/update-incident" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/update-incident', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | yes | Path parameter for identifier. |
| `incident` | object | no | Body payload field documented on https://www.reamaze.com/api/put_incident. |

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

Through the native Reamaze API, this operation is `PUT /incidents/:identifier` (base URL `https://{{credentials.brand}}.reamaze.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-incident.md) for the provider-specific parameters and requirements.

