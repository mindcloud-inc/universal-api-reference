# Trust: List Widgets

Retrieves testimonial widgets from Trust.

```
GET https://connect.mindcloud.co/v1/universal/trust/latest/actions/list-widgets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trust `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trust/latest/actions/list-widgets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trust/latest/actions/list-widgets?${params}`, {
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
      "testimonialWidgets": [
        {
          "active": true,
          "description": "string",
          "name": "Ava Chen",
          "type": "string",
          "widgetId": "string",
          "workspaceId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `testimonialWidgets` | array<object> |  |
| `testimonialWidgets[].active` | boolean |  |
| `testimonialWidgets[].description` | string |  |
| `testimonialWidgets[].name` | string |  |
| `testimonialWidgets[].type` | string |  |
| `testimonialWidgets[].widgetId` | string |  |
| `testimonialWidgets[].workspaceId` | string |  |

## Native endpoint

Through the native Trust API, this operation is `GET /widgets` (base URL `https://api.usetrust.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-widgets.md) for the provider-specific parameters and requirements.

