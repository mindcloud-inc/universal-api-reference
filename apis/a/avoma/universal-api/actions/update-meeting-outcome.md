# Avoma: Update Meeting Outcome

Updates an existing meeting outcome in Avoma.

```
PUT https://connect.mindcloud.co/v1/universal/avoma/latest/actions/update-meeting-outcome
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avoma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/update-meeting-outcome" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avoma/latest/actions/update-meeting-outcome', {
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
| `uuid` | string | yes | Unique ID of the meeting outcome. |
| `label` | string | no | Updated label of the meeting outcome. |
| `description` | string | no | Updated description of the meeting outcome. |

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

Through the native Avoma API, this operation is `PATCH /v1/meeting_outcome/:uuid/` (base URL `https://api.avoma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-meeting-outcome.md) for the provider-specific parameters and requirements.

