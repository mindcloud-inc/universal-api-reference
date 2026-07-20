# Microsoft Power BI: Imports GetImportsAsAdmin



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-imports-getimports-as-admin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-imports-getimports-as-admin?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-imports-getimports-as-admin?${params}`, {
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
| `_expand` | string | no | Expands related entities inline |
| `_filter` | string | no | Returns a subset of a results based on Odata filter query parameter condition. |
| `_skip` | number | no | Skips the first n results |
| `_top` | number | no | Returns only the first n results |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET admin/imports` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/admin-imports-getimports-as-admin.md) for the provider-specific parameters and requirements.

