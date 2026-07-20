# BaseLinker: Create Package

Creates a shipping package in BaseLinker.

```
POST https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/create-package
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BaseLinker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/create-package" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "order_id": 1,
  "courier_code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/create-package', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "order_id": 1,
    "courier_code": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `order_id` | number | yes |  |
| `courier_code` | string | yes |  |
| `account_id` | number | no |  |
| `fields[]` | array<object> | no |  |
| `packages[]` | array<object> | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parameters` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BaseLinker API returns.

## Native endpoint

Through the native BaseLinker API, this operation is `POST /connector.php` (base URL `https://api.baselinker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-package.md) for the provider-specific parameters and requirements.

