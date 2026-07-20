# Prembly: Create Custom Package

Creates a custom package in Prembly.

```
POST https://connect.mindcloud.co/v1/universal/prembly/latest/actions/create-custom-package
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/create-custom-package" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prembly/latest/actions/create-custom-package', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `POST /api/v1/api/bgc/packages/` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-package.md) for the provider-specific parameters and requirements.

