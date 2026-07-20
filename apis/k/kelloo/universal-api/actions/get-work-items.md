# Kelloo: Get Work Items

Retrieves work items from Kelloo.

```
GET https://connect.mindcloud.co/v1/universal/kelloo/latest/actions/get-work-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kelloo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kelloo/latest/actions/get-work-items?connectionId=$CONNECTION_ID&scenarioId=430" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scenarioId": "430"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kelloo/latest/actions/get-work-items?${params}`, {
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
| `scenarioId` | string | yes | The Kelloo scenario ID whose work items should be returned. Example: `430`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kelloo API returns.

## Native endpoint

Through the native Kelloo API, this operation is `GET /WorkItem` (base URL `https://plan.kelloo.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-work-items.md) for the provider-specific parameters and requirements.

