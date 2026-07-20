# Quilia: List Cases



```
GET https://connect.mindcloud.co/v1/universal/quilia/latest/actions/list-cases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quilia `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quilia/latest/actions/list-cases?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quilia/latest/actions/list-cases?${params}`, {
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
| `filter.client_id` | string | no | Filter by client_id. See endpoint description for syntax. |
| `filter.client_name` | string | no | Filter by client_name. See endpoint description for syntax. |
| `filter.status` | string | no | Filter by status. See endpoint description for syntax. |
| `filter.type` | string | no | Filter by type. See endpoint description for syntax. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Quilia API returns.

## Native endpoint

Through the native Quilia API, this operation is `GET cases` (base URL `https://api.quilia.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-cases.md) for the provider-specific parameters and requirements.

