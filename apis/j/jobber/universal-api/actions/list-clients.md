# Jobber: List Clients



```
GET https://connect.mindcloud.co/v1/universal/jobber/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jobber `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jobber/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jobber/latest/actions/list-clients?${params}`, {
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
| `columns` | string | no | Select the Jobber client fields to return. Example: `['id', 'createdAt'...]`. |
| `createdAfter` | string | no | Only return clients created after this timestamp (ISO 8601). Maps to filter.createdAt.after on the Jobber clients query. |
| `createdBefore` | string | no | Only return clients created before this timestamp (ISO 8601). Maps to filter.createdAt.before on the Jobber clients query. |
| `updatedAfter` | string | no | Only return clients updated after this timestamp (ISO 8601). Maps to filter.updatedAt.after on the Jobber clients query. |
| `updatedBefore` | string | no | Only return clients updated before this timestamp (ISO 8601). Maps to filter.updatedAt.before on the Jobber clients query. |
| `searchTerm` | string | no | Only return clients matching this Jobber search term. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jobber API returns.

## Native endpoint

Through the native Jobber API, this operation is `POST graphql` (base URL `https://api.getjobber.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

