# Qlik: Get Item

Retrieves an item from your Qlik tenant.

```
GET https://connect.mindcloud.co/v1/universal/qlik/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/get-item?connectionId=$CONNECTION_ID&itemId=65b8f2a1f4b0c2d3e4f56789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "65b8f2a1f4b0c2d3e4f56789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qlik/latest/actions/get-item?${params}`, {
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
| `itemId` | string | yes | Qlik item ID. Example: `65b8f2a1f4b0c2d3e4f56789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "ownerId": "string",
      "resourceType": "string",
      "spaceId": "string",
      "tenantId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `ownerId` | string |  |
| `resourceType` | string |  |
| `spaceId` | string |  |
| `tenantId` | string |  |

## Native endpoint

Through the native Qlik API, this operation is `GET /api/v1/items/:itemId` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

