# Kladana: Get Service

Retrieves a service record from Kladana.

```
GET https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kladana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-service?connectionId=$CONNECTION_ID&id=7944ef04-f831-11e5-7a69-971500188b19" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "7944ef04-f831-11e5-7a69-971500188b19"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-service?${params}`, {
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
| `id` | string | yes | Kladana service ID from the Service resource URL. Example: `7944ef04-f831-11e5-7a69-971500188b19`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "buyPrice": {},
      "code": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "externalCode": "string",
      "id": "string",
      "meta": {},
      "name": "Ava Chen",
      "pathName": "Ava Chen",
      "salePrices": [
        {}
      ],
      "shared": true,
      "uom": {},
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the service is archived. |
| `buyPrice` | object | Buy price. |
| `code` | string | Internal code. |
| `created` | date | Creation timestamp. |
| `description` | string | Service description. |
| `externalCode` | string | External code. |
| `id` | string | Service UUID. |
| `meta` | object | Kladana metadata reference. |
| `name` | string | Service name. |
| `pathName` | string | Folder path name. |
| `salePrices` | array<object> | Sale prices. |
| `shared` | boolean | Whether the service is shared. |
| `uom` | object | Unit of measure. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Kladana API, this operation is `GET /entity/service/{id}` (base URL `https://api.kladana.com/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service.md) for the provider-specific parameters and requirements.

