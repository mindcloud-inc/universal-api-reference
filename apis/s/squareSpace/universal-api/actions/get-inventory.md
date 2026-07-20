# SquareSpace: Get Inventory

Retrieves inventory from Squarespace by ID.

```
GET https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/get-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SquareSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/get-inventory?connectionId=$CONNECTION_ID&ids=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/get-inventory?${params}`, {
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
| `ids` | string | yes | Inventory variant IDs (comma-separated). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inventory": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inventory` | array<object> |  |

## Native endpoint

Through the native SquareSpace API, this operation is `GET /1.0/commerce/inventory/:ids` (base URL `https://api.squarespace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inventory.md) for the provider-specific parameters and requirements.

