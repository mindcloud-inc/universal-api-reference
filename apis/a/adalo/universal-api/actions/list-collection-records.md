# Adalo: List Collection Records

Retrieves records from a specific Adalo collection.

```
GET https://connect.mindcloud.co/v1/universal/adalo/latest/actions/list-collection-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adalo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adalo/latest/actions/list-collection-records?connectionId=$CONNECTION_ID&limit=25&offset=0&appId=string&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "appId": "string",
  "collectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adalo/latest/actions/list-collection-records?${params}`, {
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
| `appId` | string | yes | The Adalo app ID that owns the collection. |
| `collectionId` | string | yes | The collection ID to read records from. |
| `filterKey` | string | no | Optional single-value collection field to filter by. Use Number, Text, Boolean, or Date properties only. |
| `filterValue` | string | no | Optional value for the filter field. Must match the selected single-value property format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Adalo API returns.

## Native endpoint

Through the native Adalo API, this operation is `GET /v0/apps/:appId/collections/:collectionId` (base URL `https://api.adalo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-collection-records.md) for the provider-specific parameters and requirements.

