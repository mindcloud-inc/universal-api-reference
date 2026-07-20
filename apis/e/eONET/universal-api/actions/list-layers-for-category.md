# EONET: List Layers for Category

Retrieves layers for a category from EONET.

```
GET https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-layers-for-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EONET `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-layers-for-category?connectionId=$CONNECTION_ID&categoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "categoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-layers-for-category?${params}`, {
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
| `categoryId` | string | yes | Category ID such as wildfires or volcanoes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "layers": [
        {
          "name": "Ava Chen",
          "parameters": [
            {}
          ],
          "serviceTypeId": "string",
          "serviceUrl": "https://example.com"
        }
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `layers` | array<object> |  |
| `layers[].name` | string |  |
| `layers[].parameters` | array<object> |  |
| `layers[].serviceTypeId` | string |  |
| `layers[].serviceUrl` | string |  |
| `title` | string |  |

## Native endpoint

Through the native EONET API, this operation is `GET /layers/:categoryId` (base URL `https://eonet.gsfc.nasa.gov/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-layers-for-category.md) for the provider-specific parameters and requirements.

