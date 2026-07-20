# 2Smart Cloud: List sensors info



```
GET https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-vendor-sensors-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-vendor-sensors-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-vendor-sensors-info?${params}`, {
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
| `product_version_id` | number | no | ID of product version |
| `language` | string | no | Language of info |
| `sensor` | string | no | Topic of sensor |
| `search` | string | no | Search for entity |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "description": "string",
      "id": 1,
      "language": "string",
      "possible_value": "string",
      "product_id": 1,
      "sensor": "string",
      "title": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `description` | string |  |
| `id` | number |  |
| `language` | string |  |
| `possible_value` | string |  |
| `product_id` | number |  |
| `sensor` | string |  |
| `title` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `GET /vendor/sensors-info` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vendor-sensors-info.md) for the provider-specific parameters and requirements.

