# KIS: List Records

Retrieves all records from a KIS data table.

```
GET https://connect.mindcloud.co/v1/universal/kIS/latest/actions/list-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KIS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kIS/latest/actions/list-records?connectionId=$CONNECTION_ID&collectionName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kIS/latest/actions/list-records?${params}`, {
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
| `collectionName` | string | yes | Exact KIS table name to query. |
| `limit` | number | no | Maximum number of records to return. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native KIS API returns.

## Native endpoint

Through the native KIS API, this operation is `POST /api_token_access/data_handlers` (base URL `https://api.getkis.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-records.md) for the provider-specific parameters and requirements.

