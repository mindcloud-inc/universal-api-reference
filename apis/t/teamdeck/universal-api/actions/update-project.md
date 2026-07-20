# Teamdeck: Update Project

Updates an existing project in Teamdeck.

```
PUT https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamdeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The Teamdeck project ID. |
| `name` | string | yes |  |
| `color` | string | no |  |
| `archived` | boolean | no |  |
| `enableTimeEntryApproval` | boolean | no |  |
| `defaultApproverId` | number | no |  |
| `organizationUnitId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "color": "string",
      "createdAt": "string",
      "defaultApproverId": 1,
      "enableTimeEntryApproval": 1,
      "id": 1,
      "name": "Ava Chen",
      "organizationUnitId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `color` | string |  |
| `createdAt` | string |  |
| `defaultApproverId` | number |  |
| `enableTimeEntryApproval` | number |  |
| `id` | number |  |
| `name` | string |  |
| `organizationUnitId` | number |  |

## Native endpoint

Through the native Teamdeck API, this operation is `PUT /projects/:id` (base URL `https://api.teamdeck.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

