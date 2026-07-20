# Storyscale: Update Library Asset



```
PUT https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/update-library-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storyscale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/update-library-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/update-library-asset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Storyscale library asset ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Updated library asset payload returned by Storyscale. |
| `status` | object | Top-level API status object. |

## Native endpoint

Through the native Storyscale API, this operation is `PUT /v1/library/update/{id}` (base URL `https://prodapi.storyscale.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-library-asset.md) for the provider-specific parameters and requirements.

