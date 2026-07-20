# Stackby: List Views

Retrieves views from a Stackby table.

```
GET https://connect.mindcloud.co/v1/universal/stackby/latest/actions/list-views
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackby `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackby/latest/actions/list-views?connectionId=$CONNECTION_ID&stackId=string&tableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stackId": "string",
  "tableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackby/latest/actions/list-views?${params}`, {
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
      "name": "Ava Chen",
      "tableId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | View ID. |
| `name` | string | View name. |
| `tableId` | string | Table ID for the view. |

## Native endpoint

Through the native Stackby API, this operation is `GET /v0/viewlist/{{stackId}}/{{tableId}}` (base URL `https://stackby.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-views.md) for the provider-specific parameters and requirements.

