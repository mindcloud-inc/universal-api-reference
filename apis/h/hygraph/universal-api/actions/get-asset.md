# Hygraph: Get Asset

Retrieves an asset from Hygraph.

```
GET https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/get-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hygraph `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/get-asset?connectionId=$CONNECTION_ID&variables=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/get-asset?${params}`, {
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
| `variables` | object | yes | Required variables: id. Optional: stage. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "asset": {
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
| `data.asset` | object | Asset returned by the Hygraph Content API. |
| `data.asset.createdAt` | date | Asset creation timestamp. |
| `data.asset.fileName` | string | Asset file name. |
| `data.asset.handle` | string | Hygraph asset handle. |
| `data.asset.id` | string | Asset ID. |
| `data.asset.mimeType` | string | Asset MIME type. |
| `data.asset.size` | number | Asset size. |
| `data.asset.updatedAt` | date | Asset update timestamp. |
| `data.asset.url` | string | Asset URL. |
| `extensions` | object | Optional GraphQL response extensions. |

## Native endpoint

Through the native Hygraph API, this operation is `POST` (base URL `{{credentials.endpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset.md) for the provider-specific parameters and requirements.

