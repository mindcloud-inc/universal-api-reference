# IntakeQ: Update Practitioner

Updates an existing practitioner in IntakeQ.

```
PUT https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/update-practitioner
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/update-practitioner" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com",
  "roleName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/update-practitioner', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "firstName": "Ava",
    "lastName": "Chen",
    "email": "ava@example.com",
    "roleName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The practitioner ID. |
| `firstName` | string | yes | The practitioner's first name. |
| `lastName` | string | yes | The practitioner's last name. |
| `email` | string | yes | The practitioner's email address. |
| `roleName` | string | yes | The IntakeQ role name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completeName": "Ava Chen",
      "email": "ava@example.com",
      "externalPractitionerId": "string",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "roleName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completeName` | string |  |
| `email` | string |  |
| `externalPractitionerId` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `roleName` | string |  |

## Native endpoint

Through the native IntakeQ API, this operation is `PUT /practitioners` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-practitioner.md) for the provider-specific parameters and requirements.

