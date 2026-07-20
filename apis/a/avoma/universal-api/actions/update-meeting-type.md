# Avoma: Update Meeting Type

Updates an existing meeting type in Avoma.

```
PUT https://connect.mindcloud.co/v1/universal/avoma/latest/actions/update-meeting-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avoma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/update-meeting-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avoma/latest/actions/update-meeting-type', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuid` | string | yes | Unique ID of the meeting type. |
| `label` | string | no | Updated label of the meeting type. |
| `description` | string | no | Updated description of the meeting type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "label": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `label` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Avoma API, this operation is `PATCH /v1/meeting_type/:uuid/` (base URL `https://api.avoma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-meeting-type.md) for the provider-specific parameters and requirements.

