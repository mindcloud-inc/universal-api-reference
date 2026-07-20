# Agilite: Assign BPM Role

Assigns a role to a BPM record in Agilite.

```
PUT https://connect.mindcloud.co/v1/universal/agilite/latest/actions/assign-bpm-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agilite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/agilite/latest/actions/assign-bpm-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bpmRecordId": "string",
  "currentUser": "string",
  "roleName": "Ava Chen",
  "responsibleUsers": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agilite/latest/actions/assign-bpm-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bpmRecordId": "string",
    "currentUser": "string",
    "roleName": "Ava Chen",
    "responsibleUsers": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bpmRecordId` | string | yes | BPM record identifier. |
| `currentUser` | string | yes | Name, email, or ID of the user assigning the BPM role. |
| `roleName` | string | yes | BPM role to assign. |
| `responsibleUsers` | string | yes | Users responsible for the role assignment. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agilite API returns.

## Native endpoint

Through the native Agilite API, this operation is `GET /bpm/assignRole` (base URL `https://api.agilite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-bpm-role.md) for the provider-specific parameters and requirements.

