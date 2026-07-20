# CleverReach: Get Group Filter

Retrieves a group filter from CleverReach.

```
GET https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/get-group-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CleverReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/get-group-filter?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/get-group-filter?${params}`, {
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
| `groupId` | string | no | Group ID. |
| `filterId` | string | no | Filter ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CleverReach API returns.

## Native endpoint

Through the native CleverReach API, this operation is `GET /v3/groups.json/:groupId/filters/:filterId` (base URL `https://rest.cleverreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group-filter.md) for the provider-specific parameters and requirements.

