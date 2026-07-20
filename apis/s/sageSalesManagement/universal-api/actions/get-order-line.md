# Sage Sales Management: Get Order Line

Retrieves an order line from Sage Sales Management.

```
GET https://connect.mindcloud.co/v1/universal/sageSalesManagement/latest/actions/get-order-line
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sage Sales Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sageSalesManagement/latest/actions/get-order-line?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sageSalesManagement/latest/actions/get-order-line?${params}`, {
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
| `id` | string | yes | Order line ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Order line ID |

## Native endpoint

Through the native Sage Sales Management API, this operation is `GET /salesordersLines/{{id}}` (base URL `https://api.forcemanager.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-line.md) for the provider-specific parameters and requirements.

