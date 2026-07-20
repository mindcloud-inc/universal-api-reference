# Hygraph: List Assets

Retrieves assets from Hygraph.

```
GET https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/list-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hygraph `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/list-assets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/list-assets?${params}`, {
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
| `variables` | object | no | Optional variables: first, skip, stage. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "assets": [
          {
            "createdAt": "2026-05-07T12:00:00.000Z",
            "fileName": "Ava Chen",
            "handle": "string",
            "id": "string",
            "mimeType": "string",
            "size": 1,
            "updatedAt": "2026-05-07T12:00:00.000Z",
            "url": "https://example.com"
          }
        ]
      },
      "extensions": {
        "Complexity-Cost-Left": 1,
        "Effective-Complexity-Limit": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.assets` | array<object> | Assets returned by the Hygraph Content API. |
| `data.assets[].createdAt` | date | Asset creation timestamp. |
| `data.assets[].fileName` | string | Asset file name. |
| `data.assets[].handle` | string | Hygraph asset handle. |
| `data.assets[].id` | string | Asset ID. |
| `data.assets[].mimeType` | string | Asset MIME type. |
| `data.assets[].size` | number | Asset size. |
| `data.assets[].updatedAt` | date | Asset update timestamp. |
| `data.assets[].url` | string | Asset URL. |
| `extensions.Complexity-Cost-Left` | number | Remaining GraphQL complexity budget returned by Hygraph. |
| `extensions.Effective-Complexity-Limit` | number | Effective GraphQL complexity limit returned by Hygraph. |

## Native endpoint

Through the native Hygraph API, this operation is `POST` (base URL `{{credentials.endpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-assets.md) for the provider-specific parameters and requirements.

