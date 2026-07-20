# Timizer: Create Team Mission

Creates a team mission in Timizer.

```
POST https://connect.mindcloud.co/v1/universal/timizer/latest/actions/create-team-mission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timizer/latest/actions/create-team-mission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timizer/latest/actions/create-team-mission', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | number | yes | ID of the team. |
| `name` | string | no | Name of the mission. |
| `type` | list | no | Mission type. One of: `mission`, `project`. |
| `id` | number | no | Optional mission ID. |
| `customId` | string | no | Optional mission custom ID. |
| `clientId` | number | no | ID of the client. |
| `clientContactId` | number | no | Optional client contact ID. |
| `contractClientId` | number | no | Optional contract client ID. |
| `contractClientContactId` | number | no | Optional contract client contact ID. |
| `teamMemberLinkIds[]` | array<number> | no | Team member link IDs assigned to the mission. |
| `start` | date | no | Optional mission start datetime. |
| `end` | date | no | Optional mission end datetime. |
| `durationType` | list | no | Duration type for the mission. One of: `day`, `hour`. |
| `durationValue` | number | no | Duration value. In seconds when durationType is hour. |
| `availableTagIds[]` | array<number> | no | Tag IDs available on the mission. |
| `isActive` | boolean | no | Whether the mission is active. |
| `clientSignatureRequired` | boolean | no | Whether client signature is required. |
| `additionalReceiver` | string | no | Optional email address receiving signed activity reports. |
| `purchaseOrder` | string | no | Optional purchase order reference. |
| `note` | string | no | Optional mission note. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalReceiver": "string",
      "allowActivityReportsSharing": true,
      "client": {},
      "clientSignatureRequired": true,
      "contractClient": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customId": "string",
      "dailyCostCent": 1,
      "dailyRateCent": 1,
      "durationType": "string",
      "durationValue": 1,
      "end": "2026-05-07T12:00:00.000Z",
      "forfaitCostCent": 1,
      "hourlyCostCent": 1,
      "hourlyRateCent": 1,
      "id": 1,
      "isActive": true,
      "name": "Ava Chen",
      "note": "string",
      "parentId": 1,
      "purchaseOrder": "string",
      "remainingDurationValue": 1,
      "start": "2026-05-07T12:00:00.000Z",
      "tags": [
        {}
      ],
      "teamMemberLinks": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalReceiver` | string |  |
| `allowActivityReportsSharing` | boolean |  |
| `client` | object |  |
| `clientSignatureRequired` | boolean |  |
| `contractClient` | object |  |
| `createdAt` | date |  |
| `customId` | string |  |
| `dailyCostCent` | number |  |
| `dailyRateCent` | number |  |
| `durationType` | string |  |
| `durationValue` | number |  |
| `end` | date |  |
| `forfaitCostCent` | number |  |
| `hourlyCostCent` | number |  |
| `hourlyRateCent` | number |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `name` | string |  |
| `note` | string |  |
| `parentId` | number |  |
| `purchaseOrder` | string |  |
| `remainingDurationValue` | number |  |
| `start` | date |  |
| `tags` | array<object> |  |
| `teamMemberLinks` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native Timizer API, this operation is `POST /app/admin-teams/:teamId/missions` (base URL `https://api.timizer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-team-mission.md) for the provider-specific parameters and requirements.

