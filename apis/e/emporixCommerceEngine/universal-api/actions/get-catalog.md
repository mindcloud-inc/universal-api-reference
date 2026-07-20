# Emporix Commerce Engine: Get Catalog

Retrieves a catalog from Emporix Commerce Engine.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-catalog
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-catalog?connectionId=$CONNECTION_ID&catalogId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "catalogId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-catalog?${params}`, {
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
| `catalogId` | string | yes | The unique ID of the catalog. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryIds": [
        "string"
      ],
      "description": "string",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "publishedSites": [
        "string"
      ],
      "status": "string",
      "visibility": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryIds` | array<string> |  |
| `description` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `publishedSites` | array<string> |  |
| `status` | string |  |
| `visibility` | object |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `GET /catalog/{{credentials.tenantId}}/catalogs/:catalogId` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-catalog.md) for the provider-specific parameters and requirements.

