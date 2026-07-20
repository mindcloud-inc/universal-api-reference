# Hygraph: Update Asset Remote URL

Updates an existing asset from a remote URL in Hygraph.

```
PUT https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/update-asset-remote-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hygraph `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/update-asset-remote-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/update-asset-remote-url', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | yes | Required variables: id, uploadUrl. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "updateAsset": {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "fileName": "Ava Chen",
          "handle": "string",
          "id": "string",
          "mimeType": "string",
          "size": 1,
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "url": "https://example.com"
        }
      },
      "extensions": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.updateAsset` | object | Updated asset returned by Hygraph. |
| `data.updateAsset.createdAt` | date | Asset creation timestamp. |
| `data.updateAsset.fileName` | string | Asset file name. |
| `data.updateAsset.handle` | string | Hygraph asset handle. |
| `data.updateAsset.id` | string | Asset ID. |
| `data.updateAsset.mimeType` | string | Asset MIME type. |
| `data.updateAsset.size` | number | Asset size. |
| `data.updateAsset.updatedAt` | date | Asset update timestamp. |
| `data.updateAsset.url` | string | Asset URL. |
| `extensions` | object | Optional GraphQL response extensions. |

## Native endpoint

Through the native Hygraph API, this operation is `POST` (base URL `{{credentials.endpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-asset-remote-url.md) for the provider-specific parameters and requirements.

