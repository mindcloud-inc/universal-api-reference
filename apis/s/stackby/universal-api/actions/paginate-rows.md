# Stackby: Paginate Rows

Retrieves paginated rows from a Stackby table.

```
GET https://connect.mindcloud.co/v1/universal/stackby/latest/actions/paginate-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackby `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackby/latest/actions/paginate-rows?connectionId=$CONNECTION_ID&stackId=string&tableName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stackId": "string",
  "tableName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackby/latest/actions/paginate-rows?${params}`, {
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
| `stackId` | string | yes | Stack identifier from Stackby. |
| `tableName` | string | yes | Table name from Stackby. |
| `pageSize` | number | no | Maximum rows returned in this page. |
| `offset` | number | no | Row offset for pagination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field": {},
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field` | object | Row field values keyed by column name. |
| `id` | string | Row ID. |

## Native endpoint

Through the native Stackby API, this operation is `GET /betav1/rowlist/{{stackId}}/{{tableName}}` (base URL `https://stackby.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/paginate-rows.md) for the provider-specific parameters and requirements.

