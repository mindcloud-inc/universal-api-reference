# 2Smart Cloud: All products (in production status) schemas with each major latest versions



```
POST https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-public-schemas-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-public-schemas-versions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-public-schemas-versions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vendor_id[]` | array<number> | no | ID of vendor |
| `product_id[]` | array<number> | no | IDs of products |

## Response

```json
{
  "success": true,
  "data": [
    {
      "product_id": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `product_id` | object |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `POST /public/schemas-versions` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-public-schemas-versions.md) for the provider-specific parameters and requirements.

