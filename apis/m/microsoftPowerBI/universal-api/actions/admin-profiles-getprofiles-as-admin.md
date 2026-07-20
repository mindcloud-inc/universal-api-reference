# Microsoft Power BI: Profiles GetProfilesAsAdmin



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-profiles-getprofiles-as-admin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-profiles-getprofiles-as-admin?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-profiles-getprofiles-as-admin?${params}`, {
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
| `_filter` | string | no | Filters the results based on a boolean condition, using 'id', 'displayName', or 'servicePrincipalId'. Supports only 'eq' operator. |
| `_skip` | number | no | Skips the first n results. Use with top to fetch results beyond the first 5000. |
| `_top` | number | no | Returns only the first n results. This parameter must be in the range of 1-5000. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET admin/profiles` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/admin-profiles-getprofiles-as-admin.md) for the provider-specific parameters and requirements.

