# Timing: Show Latest Time Entry

Retrieves the latest time entry from Timing.

```
GET https://connect.mindcloud.co/v1/universal/timing/latest/actions/show-latest-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timing/latest/actions/show-latest-time-entry?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timing/latest/actions/show-latest-time-entry?${params}`, {
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
      "billingStatus": "string",
      "creatorId": "string",
      "creatorName": "Ava Chen",
      "customFields": {},
      "duration": 1,
      "endDate": "2026-05-07T12:00:00.000Z",
      "isRunning": true,
      "notes": "string",
      "project": {
        "self": "string"
      },
      "self": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingStatus` | string |  |
| `creatorId` | string |  |
| `creatorName` | string |  |
| `customFields` | object |  |
| `duration` | number |  |
| `endDate` | date |  |
| `isRunning` | boolean |  |
| `notes` | string |  |
| `project` | object |  |
| `project.self` | string |  |
| `self` | string |  |
| `startDate` | date |  |
| `title` | string |  |

## Native endpoint

Through the native Timing API, this operation is `GET /time-entries/latest` (base URL `https://web.timingapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-latest-time-entry.md) for the provider-specific parameters and requirements.

