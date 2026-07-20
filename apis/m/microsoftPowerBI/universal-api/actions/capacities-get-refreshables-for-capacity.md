# Microsoft Power BI: Get Refreshables For Capacity



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/capacities-get-refreshables-for-capacity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/capacities-get-refreshables-for-capacity?connectionId=$CONNECTION_ID&capacityId=string&_top=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "capacityId": "string",
  "_top": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/capacities-get-refreshables-for-capacity?${params}`, {
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
| `capacityId` | string | yes | The capacity ID |
| `_top` | number | yes | Returns only the first n results. |
| `_expand` | string | no | Accepts a comma-separated list of data types, which will be expanded inline in the response. Supports capacities and groups. |
| `_filter` | string | no | Returns a subset of a results based on Odata filter query parameter condition. |
| `_skip` | number | no | Skips the first n results. Use with top to fetch results beyond the first 1000. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET capacities/[:capacityId]/refreshables` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/capacities-get-refreshables-for-capacity.md) for the provider-specific parameters and requirements.

