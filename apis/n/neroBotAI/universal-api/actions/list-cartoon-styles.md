# NeroBot AI: List Cartoon Styles

Retrieves cartoon styles from NeroBot AI.

```
GET https://connect.mindcloud.co/v1/universal/neroBotAI/latest/actions/list-cartoon-styles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeroBot AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neroBotAI/latest/actions/list-cartoon-styles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neroBotAI/latest/actions/list-cartoon-styles?${params}`, {
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
            "id": "string",
            "image": "string",
            "name": "Ava Chen"
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
| `data.styles[].id` | string |  |
| `data.styles[].image` | string |  |
| `data.styles[].name` | string |  |

## Native endpoint

Through the native NeroBot AI API, this operation is `GET /biz/api/cartoon/styles` (base URL `https://api.nero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cartoon-styles.md) for the provider-specific parameters and requirements.

