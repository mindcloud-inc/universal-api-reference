# Microsoft Power BI: Get Refreshable For Capacity



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/capacities-get-refreshable-for-capacity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/capacities-get-refreshable-for-capacity?connectionId=$CONNECTION_ID&capacityId=string&refreshableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "capacityId": "string",
  "refreshableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/capacities-get-refreshable-for-capacity?${params}`, {
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
| `refreshableId` | string | yes | The refreshable ID |
| `_expand` | string | no | Accepts a comma-separated list of data types, which will be expanded inline in the response. Supports capacities and groups. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET capacities/[:capacityId]/refreshables/[:refreshableId]` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/capacities-get-refreshable-for-capacity.md) for the provider-specific parameters and requirements.

