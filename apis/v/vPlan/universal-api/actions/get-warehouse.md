# vPlan: Get Warehouse



```
GET https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-warehouse
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-warehouse?connectionId=$CONNECTION_ID&id=475c382b-debc-42e8-812b-0207075a7bbf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "475c382b-debc-42e8-812b-0207075a7bbf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-warehouse?${params}`, {
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
| `id` | string | yes | Warehouse identifier. Default: `475c382b-debc-42e8-812b-0207075a7bbf`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "created_at": "string",
      "external_ref": "string",
      "id": "string",
      "name": "Ava Chen",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Warehouse code. |
| `created_at` | string | Creation timestamp. |
| `external_ref` | string | External reference. |
| `id` | string | Warehouse identifier. |
| `name` | string | Warehouse name. |
| `updated_at` | string | Last update timestamp. |

## Native endpoint

Through the native vPlan API, this operation is `GET /warehouse/[:id]` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-warehouse.md) for the provider-specific parameters and requirements.

