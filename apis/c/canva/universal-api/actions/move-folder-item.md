# Canva: Move Folder Item

Moves an item to another Canva folder.

```
PUT https://connect.mindcloud.co/v1/universal/canva/latest/actions/move-folder-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canva `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/canva/latest/actions/move-folder-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemId": "FAHDrkEuHo0",
  "toFolderId": "FAHDriNMZAE"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/canva/latest/actions/move-folder-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemId": "FAHDrkEuHo0",
    "toFolderId": "FAHDriNMZAE"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemId` | string | yes | Example: `FAHDrkEuHo0`. |
| `toFolderId` | string | yes | Example: `FAHDriNMZAE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Endpoint returned an empty response body (204 No Content). |

## Native endpoint

Through the native Canva API, this operation is `POST /v1/folders/move` (base URL `https://api.canva.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-folder-item.md) for the provider-specific parameters and requirements.

