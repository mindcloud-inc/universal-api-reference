# Strava: List Athlete Clubs

Retrieves clubs for the authenticated athlete from Strava.

```
GET https://connect.mindcloud.co/v1/universal/strava/latest/actions/list-athlete-clubs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strava `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strava/latest/actions/list-athlete-clubs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strava/latest/actions/list-athlete-clubs?${params}`, {
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
| `limit` | number | no | Number of clubs to return per page (1-200). |
| `page` | number | no | Page number to return, starting at 1. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Strava API returns.

## Native endpoint

Through the native Strava API, this operation is `GET /athlete/clubs` (base URL `https://www.strava.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-athlete-clubs.md) for the provider-specific parameters and requirements.

