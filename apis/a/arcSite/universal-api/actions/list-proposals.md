# ArcSite: List Proposals

Retrieves proposal records from your ArcSite organization.

```
GET https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/list-proposals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ArcSite `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/list-proposals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/list-proposals?${params}`, {
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
| `projectId` | string | no | Project ID to filter proposals. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ArcSite API returns.

## Native endpoint

Through the native ArcSite API, this operation is `GET /proposals` (base URL `https://api.arcsite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-proposals.md) for the provider-specific parameters and requirements.

