# Hireflix: Invite Candidate To Interview

Invites a candidate to an interview in Hireflix.

```
POST https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/invite-candidate-to-interview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hireflix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/invite-candidate-to-interview" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.input.positionId": "string",
  "variables.input.candidate.firstName": "Ava",
  "variables.input.candidate.email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/invite-candidate-to-interview', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.input.positionId": "string",
    "variables.input.candidate.firstName": "Ava",
    "variables.input.candidate.email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.input.positionId` | string | yes | The Hireflix position ID. |
| `variables.input.candidate.firstName` | string | yes | The candidate's first name. |
| `variables.input.candidate.lastName` | string | no | The candidate's last name. |
| `variables.input.candidate.email` | string | yes | The candidate's email address. |
| `variables.input.candidate.phone` | string | no | The candidate's phone number. |
| `variables.input.externalId` | string | no | An external ID to associate with the interview. |
| `variables.input.disableNotifications` | boolean | no | Whether to suppress Hireflix notifications for this invite. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.input.metadata` | object | no | Optional JSON metadata to store with the interview invite. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "__typename": "Ava Chen",
      "candidate": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "phone": "string"
      },
      "code": "string",
      "expires": 1,
      "externalId": "string",
      "fieldErrors": {},
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "position": {
        "id": "string",
        "name": "Ava Chen"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `__typename` | string |  |
| `candidate.email` | string |  |
| `candidate.firstName` | string |  |
| `candidate.lastName` | string |  |
| `candidate.phone` | string |  |
| `code` | string |  |
| `expires` | number |  |
| `externalId` | string |  |
| `fieldErrors` | object |  |
| `id` | string |  |
| `message` | string |  |
| `name` | string |  |
| `position.id` | string |  |
| `position.name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Hireflix API, this operation is `POST me` (base URL `https://api.hireflix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-candidate-to-interview.md) for the provider-specific parameters and requirements.

