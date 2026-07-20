# Woodpecker.co: List Prospects

Retrieves prospects from the Woodpecker database.

```
GET https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/list-prospects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Woodpecker.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/list-prospects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/list-prospects?${params}`, {
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
| `page` | number | no | Page number. |
| `perPage` | number | no | Number of prospects per page. |
| `sort` | string | no | Woodpecker sort expression. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Woodpecker.co API returns.

## Native endpoint

Through the native Woodpecker.co API, this operation is `GET /rest/v1/prospects` (base URL `https://api.woodpecker.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-prospects.md) for the provider-specific parameters and requirements.

