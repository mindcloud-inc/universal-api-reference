# SimpleKPI: Delete User KPI

Deletes a KPI from a SimpleKPI user.

```
DELETE https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/delete-user-kpi
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleKPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/delete-user-kpi?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/delete-user-kpi?${params}`, {
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
| `id` | number | no | The KPI ID assigned to the user. |
| `userId` | number | no | The user ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SimpleKPI API returns.

## Native endpoint

Through the native SimpleKPI API, this operation is `DELETE users/:userId/kpis/:id` (base URL `https://{{credentials.subdomain}}.simplekpi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-user-kpi.md) for the provider-specific parameters and requirements.

