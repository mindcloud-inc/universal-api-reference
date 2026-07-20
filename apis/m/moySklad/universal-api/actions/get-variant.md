# MoySklad: Get variant

Retrieves the variant from MoySklad.

```
GET https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/get-variant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoySklad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/get-variant?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/get-variant?${params}`, {
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
| `id` | string | yes | MoySklad entity id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "code": "string",
      "externalCode": "string",
      "id": "string",
      "meta": {},
      "name": "Ava Chen",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `code` | string |  |
| `externalCode` | string |  |
| `id` | string |  |
| `meta` | object |  |
| `name` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native MoySklad API, this operation is `GET entity/variant/:id` (base URL `https://api.moysklad.ru/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-variant.md) for the provider-specific parameters and requirements.

