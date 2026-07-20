# Shotstack: Get Asset



```
GET https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/get-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shotstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/get-asset?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/get-asset?${params}`, {
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
| `id` | string | yes | The Shotstack asset ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "filename": "Ava Chen",
          "id": "string",
          "renderId": "string",
          "status": "string",
          "url": "https://example.com"
        },
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.attributes.filename` | string | Asset filename. |
| `data.attributes.id` | string | Asset identifier. |
| `data.attributes.renderId` | string | Render identifier associated with the asset. |
| `data.attributes.status` | string | Current asset status. |
| `data.attributes.url` | string | Served asset URL. |
| `data.type` | string | Resource type for the asset. |

## Native endpoint

Through the native Shotstack API, this operation is `GET /serve/v1/assets/:id` (base URL `https://api.shotstack.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset.md) for the provider-specific parameters and requirements.

