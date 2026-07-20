# Qlik: Update Collection

Updates an existing collection in Qlik.

```
PUT https://connect.mindcloud.co/v1/universal/qlik/latest/actions/update-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/update-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "65b8f2a1f4b0c2d3e4f56789"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qlik/latest/actions/update-collection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "65b8f2a1f4b0c2d3e4f56789"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | Qlik collection ID. Example: `65b8f2a1f4b0c2d3e4f56789`. |
| `name` | string | no | Collection name. Example: `Executive dashboards`. |
| `description` | string | no | Collection description. Example: `Updated collection description`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "itemCount": 1,
      "name": "Ava Chen",
      "tenantId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `itemCount` | number |  |
| `name` | string |  |
| `tenantId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Qlik API, this operation is `PUT /api/v1/collections/:collectionId` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-collection.md) for the provider-specific parameters and requirements.

