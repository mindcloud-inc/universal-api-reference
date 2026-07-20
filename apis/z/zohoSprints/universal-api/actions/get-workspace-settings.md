# Zoho Sprints: Get Workspace Settings

Retrieves workspace settings from Zoho Sprints.

```
GET https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/get-workspace-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sprints `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/get-workspace-settings?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/get-workspace-settings?${params}`, {
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
| `teamId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminzuid": "string",
      "currency": "string",
      "isAPIEnabled": 1,
      "onboardingInfo": {},
      "parallelSprints": true,
      "planName": "Ava Chen",
      "profileData": {},
      "status": "string",
      "strictScrum": true,
      "teamName": "Ava Chen",
      "timesheetSettings": {},
      "timezone": "string",
      "weekStart": 1,
      "zoid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminzuid` | string |  |
| `currency` | string |  |
| `isAPIEnabled` | number |  |
| `onboardingInfo` | object |  |
| `parallelSprints` | boolean |  |
| `planName` | string |  |
| `profileData` | object |  |
| `status` | string |  |
| `strictScrum` | boolean |  |
| `teamName` | string |  |
| `timesheetSettings` | object |  |
| `timezone` | string |  |
| `weekStart` | number |  |
| `zoid` | string |  |

## Native endpoint

Through the native Zoho Sprints API, this operation is `GET /team/:teamId/settings/` (base URL `https://sprintsapi.zoho.com/zsapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace-settings.md) for the provider-specific parameters and requirements.

