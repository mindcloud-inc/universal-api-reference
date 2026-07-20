# Sigma: List Connection Table Columns



```
GET https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-connection-table-columns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sigma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-connection-table-columns?connectionId=$CONNECTION_ID&tableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-connection-table-columns?${params}`, {
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
| `tableId` | string | yes | Sigma tableId. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entries": [
        {}
      ],
      "nextPageToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entries` | array<object> | Column entries |
| `nextPageToken` | string | Cursor for the next page of columns |

## Native endpoint

Through the native Sigma API, this operation is `GET /v2/connections/tables/{tableId}/columns` (base URL `https://aws-api.sigmacomputing.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-connection-table-columns.md) for the provider-specific parameters and requirements.

