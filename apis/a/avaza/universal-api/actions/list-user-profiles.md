# Avaza: List User Profiles

Retrieves user profiles from Avaza.

```
GET https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-user-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-user-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-user-profiles?${params}`, {
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
| `roles` | string | no | Optional list of comma separated role codes to filter users by (e.g. "TimesheetUser,Admin") |
| `tags` | string | no |  |
| `currentuseronly` | boolean | no | Optional boolean (true/false) to filter to only show current authenticated user (always true for non Admin/Finance Manager users) |
| `companyidfk` | number | no | Optionally filter by Company ID |
| `email` | string | no | Optionally filter by user email address |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `GET /api/UserProfile` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-profiles.md) for the provider-specific parameters and requirements.

