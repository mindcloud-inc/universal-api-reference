# 2Smart Cloud: Show api token



```
GET https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-api-tokens-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-api-tokens-by-id?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-api-tokens-by-id?${params}`, {
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
| `id` | number | yes | ID of entity |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_token": "string",
      "created": "string",
      "id": 1,
      "name": "Ava Chen",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_token` | string |  |
| `created` | string |  |
| `id` | number |  |
| `name` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `GET /vendor/api-tokens/{id}` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vendor-api-tokens-by-id.md) for the provider-specific parameters and requirements.

