# Mixpanel: Get Profile Event Activity

Retrieves profile event activity from Mixpanel.

```
GET https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/get-profile-event-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mixpanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/get-profile-event-activity?connectionId=$CONNECTION_ID&distinctIds=user-1%2Cuser-2&fromDate=2026-03-01&toDate=2026-03-12" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "distinctIds": "user-1,user-2",
  "fromDate": "2026-03-01",
  "toDate": "2026-03-12"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/get-profile-event-activity?${params}`, {
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
| `distinctIds` | string | yes | JSON array string of distinct IDs to inspect. Example: `user-1,user-2`. |
| `fromDate` | string | yes | Inclusive start date in YYYY-MM-DD format. Example: `2026-03-01`. |
| `toDate` | string | yes | Inclusive end date in YYYY-MM-DD format. Example: `2026-03-12`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | no | Required when authenticating with a Mixpanel service account. Example: `12345`. |
| `workspaceId` | number | no | Optional Mixpanel workspace ID. Example: `98765`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": {
        "events": [
          {
            "event": "string"
          }
        ]
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results.events[].event` | string | Event name in the activity stream. |
| `status` | string | Mixpanel response status. |

## Native endpoint

Through the native Mixpanel API, this operation is `GET /query/stream/query` (base URL `https://mixpanel.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profile-event-activity.md) for the provider-specific parameters and requirements.

