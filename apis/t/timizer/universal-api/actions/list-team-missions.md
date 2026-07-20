# Timizer: List Team Missions

Retrieves team missions from Timizer.

```
GET https://connect.mindcloud.co/v1/universal/timizer/latest/actions/list-team-missions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timizer/latest/actions/list-team-missions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timizer/latest/actions/list-team-missions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `month` | string | no | Year also needs to be set if Month is used. |
| `teamId` | string | no | ID of the team. |
| `year` | string | no | Month also needs to be set if Year is used. |

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

Through the native Timizer API, this operation is `GET /app/admin-teams/:teamId/missions` (base URL `https://api.timizer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-team-missions.md) for the provider-specific parameters and requirements.

