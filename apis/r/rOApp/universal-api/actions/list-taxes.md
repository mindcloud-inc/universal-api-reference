# RO App: List Taxes



```
GET https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-taxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-taxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-taxes?${params}`, {
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
| `sort` | string | no | Defines the sorting order of returned results. Use a field name to sort ascending or prefix it with a minus sign (-) to sort descending. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branch_ids": [
        "string"
      ],
      "id": 1,
      "is_enabled": true,
      "name": "Ava Chen",
      "rate": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branch_ids` | array<string> |  |
| `id` | number |  |
| `is_enabled` | boolean |  |
| `name` | string |  |
| `rate` | string |  |
| `type` | string |  |

## Native endpoint

Through the native RO App API, this operation is `GET /company/taxes` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-taxes.md) for the provider-specific parameters and requirements.

