# NeroBot AI: List Avatar Styles

Retrieves avatar styles from NeroBot AI.

```
GET https://connect.mindcloud.co/v1/universal/neroBotAI/latest/actions/list-avatar-styles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeroBot AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neroBotAI/latest/actions/list-avatar-styles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neroBotAI/latest/actions/list-avatar-styles?${params}`, {
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
      "code": 1,
      "data": {
        "styles": [
          {
            "description": "string",
            "images": [
              "string"
            ],
            "presets": {
              "female": 1,
              "male": 1
            },
            "style_id": "string",
            "title": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | object |  |
| `data.styles[].description` | string |  |
| `data.styles[].images[]` | string |  |
| `data.styles[].presets.female` | number |  |
| `data.styles[].presets.male` | number |  |
| `data.styles[].style_id` | string |  |
| `data.styles[].title` | string |  |

## Native endpoint

Through the native NeroBot AI API, this operation is `GET /biz/api/avatar/styles` (base URL `https://api.nero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-avatar-styles.md) for the provider-specific parameters and requirements.

