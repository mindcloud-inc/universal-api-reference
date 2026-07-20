# 2Smart Cloud: List locales



```
GET https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-vendor-locales
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-vendor-locales?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-vendor-locales?${params}`, {
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
| `entity_id` | number | no | ID of product version |
| `language` | string | no | Language of locale |
| `type` | string | no | Type of locale |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "language": "string",
      "text": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `language` | string |  |
| `text` | string |  |
| `type` | string |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `GET /vendor/locales` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vendor-locales.md) for the provider-specific parameters and requirements.

