# Avaza: List Fixed Amounts

Retrieves fixed-amount entries from Avaza.

```
GET https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-fixed-amounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-fixed-amounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-fixed-amounts?${params}`, {
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
| `updatedafter` | date | no |  |
| `projectid` | number | no | (Optional) The ProjectID of a Project to filter Fixed Amounts for |
| `taskid` | number | no | (Optional) The TaskID of a Task to filter Fixed Amounts for |
| `isinvoiced` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `GET /api/FixedAmount` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-fixed-amounts.md) for the provider-specific parameters and requirements.

