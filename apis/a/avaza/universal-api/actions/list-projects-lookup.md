# Avaza: List Projects Lookup

Retrieves projects lookup entries from Avaza.

```
GET https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-projects-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-projects-lookup?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-projects-lookup?${params}`, {
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
| `timesheetuserid` | number | no | Optionally Filter to the projects that the supplied UserID can add timesheets to |
| `companyidfk` | number | no | Optionally Filter for a specific Company ID |
| `search` | string | no | Optional Search string to match against Project title and Customer name |
| `projectcode` | string | no | Optional string to exact match against Project Code |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `GET /api/Project/Lookup` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects-lookup.md) for the provider-specific parameters and requirements.

