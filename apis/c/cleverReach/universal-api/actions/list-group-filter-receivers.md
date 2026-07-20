# CleverReach: List Group Filter Receivers

Retrieves group filter receivers from CleverReach.

```
GET https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/list-group-filter-receivers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CleverReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/list-group-filter-receivers?connectionId=$CONNECTION_ID&groupId=string&filterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string",
  "filterId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/list-group-filter-receivers?${params}`, {
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
| `groupId` | string | yes | Group ID. |
| `filterId` | string | yes | Filter ID. |
| `pagesize` | number | no | Pagesize (max 5000). Default: `50`. |
| `page` | number | no | Page (zero-based). Default: `0`. |
| `type` | string | no | Type. One of: `0`, `1`, `2`, `3`. Default: `all`. |
| `detail` | number | no | Detail depth (bitwise combinable) (0: none, 1: events, 2: orders, 4: tags). Default: `0`. |
| `emailList` | string | no | list of Receiver Emails's to filter for. comma separated like: "foo@bar.com,bar@foo.com,...". |
| `idList` | string | no | list of Receiver ID's to filter for. comma separated like: "123,633,5342". |
| `orderBy` | string | no | field to order by, append 'asc' or 'desc' with a space. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CleverReach API returns.

## Native endpoint

Through the native CleverReach API, this operation is `GET /v3/groups.json/:groupId/filters/:filterId/receivers` (base URL `https://rest.cleverreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-filter-receivers.md) for the provider-specific parameters and requirements.

