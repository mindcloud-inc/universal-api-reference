# Stackby: List Columns

Retrieves columns from a Stackby table.

```
GET https://connect.mindcloud.co/v1/universal/stackby/latest/actions/list-columns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackby `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackby/latest/actions/list-columns?connectionId=$CONNECTION_ID&stackId=string&tableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stackId": "string",
  "tableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackby/latest/actions/list-columns?${params}`, {
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
| `tableId` | string | yes | Table identifier from Stackby. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "key": "string",
      "label": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Column ID. |
| `key` | string | Column key. |
| `label` | string | Column label. |
| `name` | string | Column name. |
| `type` | string | Column type. |

## Native endpoint

Through the native Stackby API, this operation is `GET /v0/columnlist/{{stackId}}/{{tableId}}` (base URL `https://stackby.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-columns.md) for the provider-specific parameters and requirements.

