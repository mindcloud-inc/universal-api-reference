# Strava: List Athlete Activities

Retrieves activities for the authenticated athlete from Strava.

```
GET https://connect.mindcloud.co/v1/universal/strava/latest/actions/list-athlete-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strava `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strava/latest/actions/list-athlete-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strava/latest/actions/list-athlete-activities?${params}`, {
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
| `before` | date | no | Only return activities that started before this epoch timestamp. |
| `after` | date | no | Only return activities that started after this epoch timestamp. |
| `limit` | number | no | Number of activities to return per page (1-200). |
| `page` | number | no | Page number to return, starting at 1. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Strava API returns.

## Native endpoint

Through the native Strava API, this operation is `GET /athlete/activities` (base URL `https://www.strava.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-athlete-activities.md) for the provider-specific parameters and requirements.

