# Dubble: List Guides

Retrieves a list of guides from Dubble.

```
GET https://connect.mindcloud.co/v1/universal/dubble/latest/actions/list-guides
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dubble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dubble/latest/actions/list-guides?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dubble/latest/actions/list-guides?${params}`, {
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
| `collection` | string | no | Filter guides by collection ID |
| `createdAfter` | string | no | Filter guides created after a date |
| `cursor` | string | no | Cursor returned from the previous page |
| `perPage` | number | no | Number of items per page |
| `search` | string | no | Search guides by title |
| `sort` | string | no | Sort direction: asc or desc |
| `updatedAfter` | string | no | Filter guides updated after a date |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dubble API returns.

## Native endpoint

Through the native Dubble API, this operation is `GET /guides` (base URL `https://api.dubble.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-guides.md) for the provider-specific parameters and requirements.

