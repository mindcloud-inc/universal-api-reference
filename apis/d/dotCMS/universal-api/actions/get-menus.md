# DotCMS: Get Menus

Retrieves available navigation menus from DotCMS.

```
GET https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/get-menus
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DotCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/get-menus?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/get-menus?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "entity": [
        {
          "id": "string",
          "menuItems": [
            {
              "ajax": true,
              "angular": true,
              "id": "string",
              "label": "string",
              "url": "https://example.com"
            }
          ],
          "name": "Ava Chen",
          "tabIcon": "string",
          "tabName": "Ava Chen",
          "url": "https://example.com"
        }
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity[].id` | string |  |
| `entity[].menuItems[].ajax` | boolean |  |
| `entity[].menuItems[].angular` | boolean |  |
| `entity[].menuItems[].id` | string |  |
| `entity[].menuItems[].label` | string |  |
| `entity[].menuItems[].url` | string |  |
| `entity[].name` | string |  |
| `entity[].tabIcon` | string |  |
| `entity[].tabName` | string |  |
| `entity[].url` | string |  |
| `pagination` | object |  |

## Native endpoint

Through the native DotCMS API, this operation is `GET /api/v1/menu` (base URL `https://demo.dotcms.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-menus.md) for the provider-specific parameters and requirements.

