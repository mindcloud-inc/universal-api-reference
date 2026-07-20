# Pinghome: Create Incident

Creates a new incident in Pinghome.

```
POST https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-incident
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-incident" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "2a85fda9-2f9b-4daf-b040-f30a835cafa5",
  "name": "MindCloud Test Incident",
  "description": "Incident created by MindCloud action test",
  "urgency": "medium"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-incident', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "2a85fda9-2f9b-4daf-b040-f30a835cafa5",
    "name": "MindCloud Test Incident",
    "description": "Incident created by MindCloud action test",
    "urgency": "medium"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | Team ID for the incident. Example: `2a85fda9-2f9b-4daf-b040-f30a835cafa5`. |
| `name` | string | yes | Incident name. Example: `MindCloud Test Incident`. |
| `description` | string | yes | Incident description. Example: `Incident created by MindCloud action test`. |
| `urgency` | string | yes | Incident urgency level. Example: `medium`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignees[]` | array<object> | no | Optional assignee definitions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "incident": {
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `incident.id` | string | Incident ID |

## Native endpoint

Through the native Pinghome API, this operation is `POST /incident-cmd/v1/team/:id/incident` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-incident.md) for the provider-specific parameters and requirements.

