# Kommo: Get Catalog Custom Field



```
GET https://connect.mindcloud.co/v1/universal/kommo/latest/actions/get-catalog-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kommo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kommo/latest/actions/get-catalog-custom-field?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kommo/latest/actions/get-catalog-custom-field?${params}`, {
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
| `custom_field_id` | string | no | Required path parameter for Get Catalog Custom Field. |
| `list_id` | string | no | Required path parameter for Get Catalog Custom Field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "id": "string",
      "links": {
        "self": {
          "href": "https://example.com"
        }
      },
      "name": "Ava Chen",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | Creation timestamp when returned by Kommo. |
| `id` | string | Unique identifier returned by Kommo. |
| `links.self.href` | string | Kommo API resource URL when returned in links. |
| `name` | string | Display name or title when returned by Kommo. |
| `updatedAt` | number | Last update timestamp when returned by Kommo. |

## Native endpoint

Through the native Kommo API, this operation is `GET /catalogs/:list_id/custom_fields/:custom_field_id` (base URL `https://{{credentials.authorizeRequest.referer}}/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-catalog-custom-field.md) for the provider-specific parameters and requirements.

