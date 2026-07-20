# Kelloo: Get Project Lookup Values

Retrieves values for a Kelloo project lookup.

```
GET https://connect.mindcloud.co/v1/universal/kelloo/latest/actions/get-project-lookup-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kelloo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kelloo/latest/actions/get-project-lookup-values?connectionId=$CONNECTION_ID&id=priority_id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "priority_id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kelloo/latest/actions/get-project-lookup-values?${params}`, {
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
| `id` | string | yes | The project lookup field identifier, such as `priority_id`. Example: `priority_id`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kelloo API returns.

## Native endpoint

Through the native Kelloo API, this operation is `GET /ProjectLookup` (base URL `https://plan.kelloo.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-lookup-values.md) for the provider-specific parameters and requirements.

