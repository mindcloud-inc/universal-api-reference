# vPlan: Get Item



```
GET https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-item?connectionId=$CONNECTION_ID&id=a7be2735-d0b1-42e6-910f-97b84b9a23d6" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "a7be2735-d0b1-42e6-910f-97b84b9a23d6"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-item?${params}`, {
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
| `id` | string | yes | Item identifier. Default: `a7be2735-d0b1-42e6-910f-97b84b9a23d6`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "created_at": "string",
      "description": "string",
      "external_ref": "string",
      "id": "string",
      "location": "string",
      "note": "string",
      "stockmanagement": true,
      "type": "string",
      "unit": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Item code. |
| `created_at` | string | Creation timestamp. |
| `description` | string | Item description. |
| `external_ref` | string | External reference. |
| `id` | string | Item identifier. |
| `location` | string | Item location. |
| `note` | string | Item note. |
| `stockmanagement` | boolean | Whether stock management is enabled. |
| `type` | string | Item type. |
| `unit` | string | Item unit. |
| `updated_at` | string | Last update timestamp. |

## Native endpoint

Through the native vPlan API, this operation is `GET /item/[:id]` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

