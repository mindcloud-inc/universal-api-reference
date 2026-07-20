# Timizer: List Teams

Retrieves teams from Timizer.

```
GET https://connect.mindcloud.co/v1/universal/timizer/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timizer/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timizer/latest/actions/list-teams?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "activityReportCustomText": "string",
      "allowActivityReportDocuments": true,
      "allowAdminsToCreateActivityReports": true,
      "allowExpenseReports": true,
      "allowHoursActivityReports": true,
      "allowNonSignedActivityReportSharing": true,
      "allowQuarterActivityReports": true,
      "areMembersRestrictedToTeamOnly": true,
      "billingType": "string",
      "brandingLogoAvailable": true,
      "brandingLogoDarkUrl": "https://example.com",
      "brandingLogoEnabled": true,
      "brandingLogoLightUrl": "https://example.com",
      "color": "string",
      "defaultClient": {},
      "defaultContracted": {},
      "forceDefaultContracted": true,
      "id": 1,
      "isActive": true,
      "logoUrl": "https://example.com",
      "name": "Ava Chen",
      "owner": {},
      "restrictActivityReportShareToLastXDays": 1,
      "totalSeatCount": 1,
      "type": "string",
      "usedSeatCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activityReportCustomText` | string |  |
| `allowActivityReportDocuments` | boolean |  |
| `allowAdminsToCreateActivityReports` | boolean |  |
| `allowExpenseReports` | boolean |  |
| `allowHoursActivityReports` | boolean |  |
| `allowNonSignedActivityReportSharing` | boolean |  |
| `allowQuarterActivityReports` | boolean |  |
| `areMembersRestrictedToTeamOnly` | boolean |  |
| `billingType` | string |  |
| `brandingLogoAvailable` | boolean |  |
| `brandingLogoDarkUrl` | string |  |
| `brandingLogoEnabled` | boolean |  |
| `brandingLogoLightUrl` | string |  |
| `color` | string |  |
| `defaultClient` | object |  |
| `defaultContracted` | object |  |
| `forceDefaultContracted` | boolean |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `logoUrl` | string |  |
| `name` | string |  |
| `owner` | object |  |
| `restrictActivityReportShareToLastXDays` | number |  |
| `totalSeatCount` | number |  |
| `type` | string |  |
| `usedSeatCount` | number |  |

## Native endpoint

Through the native Timizer API, this operation is `GET /app/admin-teams` (base URL `https://api.timizer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

