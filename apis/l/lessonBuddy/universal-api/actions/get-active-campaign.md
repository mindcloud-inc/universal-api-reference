# LessonBuddy: Get Active Campaign

Retrieves the active campaign for a location in LessonBuddy.

```
GET https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/get-active-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LessonBuddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/get-active-campaign?connectionId=$CONNECTION_ID&locationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/get-active-campaign?${params}`, {
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
| `locationId` | number | yes | LessonBuddy location ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignPhase": {},
      "endDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "startDate": "2026-05-07T12:00:00.000Z",
      "template": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignPhase` | object |  |
| `endDate` | date |  |
| `id` | number |  |
| `name` | string |  |
| `startDate` | date |  |
| `template` | object |  |

## Native endpoint

Through the native LessonBuddy API, this operation is `GET /v2/campaign/campaigns/location/:locationId/active` (base URL `https://api.lessonbuddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-active-campaign.md) for the provider-specific parameters and requirements.

