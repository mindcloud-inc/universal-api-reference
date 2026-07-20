# Beehiiv: List Subscriptions

Retrieves subscriptions from Beehiiv.

```
GET https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beehiiv `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0&publicationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "publicationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/list-subscriptions?${params}`, {
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
| `publicationId` | string | yes | The prefixed ID of the publication object. |
| `expand` | string | no | Optional list of expandable subscription objects. |
| `status` | string | no | Optional subscription status filter. |
| `tier` | string | no | Optional subscription tier filter. |
| `email` | string | no | Optional exact, case-insensitive email filter. |
| `cursor` | string | no | Cursor for cursor-based pagination. |
| `creationDate` | string | no | Filter subscriptions by creation date (YYYY/MM/DD). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beehiiv API returns.

## Native endpoint

Through the native Beehiiv API, this operation is `GET /v2/publications/:publicationId/subscriptions` (base URL `https://api.beehiiv.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

