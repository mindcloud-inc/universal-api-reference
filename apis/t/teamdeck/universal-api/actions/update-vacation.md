# Teamdeck: Update Vacation

Updates an existing vacation in Teamdeck.

```
PUT https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/update-vacation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamdeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/update-vacation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "resourceId": 1,
  "startDate": "string",
  "endDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/update-vacation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "resourceId": 1,
    "startDate": "string",
    "endDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The Teamdeck vacation ID. |
| `resourceId` | number | yes |  |
| `status` | number | no |  |
| `periodId` | number | no |  |
| `requestedApproverId` | number | no |  |
| `reasonId` | number | no |  |
| `description` | string | no |  |
| `externalId` | string | no |  |
| `startDate` | string | yes |  |
| `endDate` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approverResourceId": 1,
      "creatorResourceId": 1,
      "description": "string",
      "editorResourceId": 1,
      "endDate": "string",
      "externalId": "string",
      "id": 1,
      "periodId": 1,
      "reasonId": 1,
      "requestedApproverId": 1,
      "requestedApproverResourceId": 1,
      "resourceId": 1,
      "startDate": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approverResourceId` | number |  |
| `creatorResourceId` | number |  |
| `description` | string |  |
| `editorResourceId` | number |  |
| `endDate` | string |  |
| `externalId` | string |  |
| `id` | number |  |
| `periodId` | number |  |
| `reasonId` | number |  |
| `requestedApproverId` | number |  |
| `requestedApproverResourceId` | number |  |
| `resourceId` | number |  |
| `startDate` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Teamdeck API, this operation is `PUT /vacations/:id` (base URL `https://api.teamdeck.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-vacation.md) for the provider-specific parameters and requirements.

