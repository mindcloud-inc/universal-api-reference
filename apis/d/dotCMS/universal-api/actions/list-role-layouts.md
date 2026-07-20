# DotCMS: List Role Layouts

Retrieves role layout records from DotCMS.

```
GET https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-role-layouts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DotCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-role-layouts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-role-layouts?${params}`, {
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
          "description": "string",
          "id": "string",
          "name": "Ava Chen",
          "portletIds": [
            "string"
          ],
          "portletTitles": [
            "string"
          ],
          "tabOrder": 1
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
| `entity[].description` | string |  |
| `entity[].id` | string |  |
| `entity[].name` | string |  |
| `entity[].portletIds[]` | string |  |
| `entity[].portletTitles[]` | string |  |
| `entity[].tabOrder` | number |  |
| `pagination` | object |  |

## Native endpoint

Through the native DotCMS API, this operation is `GET /api/v1/roles/layouts` (base URL `https://demo.dotcms.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-role-layouts.md) for the provider-specific parameters and requirements.

