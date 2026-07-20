# IntakeQ: Update Assistant

Updates an existing assistant in IntakeQ.

```
PUT https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/update-assistant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/update-assistant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/update-assistant', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "externalAssistantId": "string",
      "id": "string",
      "name": "Ava Chen",
      "practitionerIds": [
        "string"
      ],
      "roleName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `externalAssistantId` | string |  |
| `id` | string |  |
| `name` | string |  |
| `practitionerIds` | array<string> |  |
| `roleName` | string |  |

## Native endpoint

Through the native IntakeQ API, this operation is `PUT /assistants` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-assistant.md) for the provider-specific parameters and requirements.

