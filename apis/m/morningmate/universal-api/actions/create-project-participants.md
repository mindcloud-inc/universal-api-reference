# Morningmate: Create Project Participants

Adds participants to a Morningmate project.

```
PUT https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/create-project-participants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morningmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/create-project-participants" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "267479",
  "registerId": "apps@mindcloud.co",
  "participants[]": [
    {}
  ],
  "participants[].participantId": "colleague@company.name"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/create-project-participants', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "267479",
    "registerId": "apps@mindcloud.co",
    "participants[]": [{}],
    "participants[].participantId": "colleague@company.name"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | Morningmate numeric project ID Example: `267479`. |
| `registerId` | string | yes | Morningmate author user ID Example: `apps@mindcloud.co`. |
| `participants[]` | array<object> | yes | Participants array |
| `participants[].participantId` | string | yes | Participant ID to add Example: `colleague@company.name`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "projectId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `projectId` | string |  |

## Native endpoint

Through the native Morningmate API, this operation is `POST /v1/projects/[:projectId]/participants` (base URL `https://api.morningmate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-participants.md) for the provider-specific parameters and requirements.

