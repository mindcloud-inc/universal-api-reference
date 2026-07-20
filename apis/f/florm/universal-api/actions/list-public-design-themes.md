# Florm: List Public Design Themes

Retrieves public design themes from Florm.

```
GET https://connect.mindcloud.co/v1/universal/florm/latest/actions/list-public-design-themes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Florm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/florm/latest/actions/list-public-design-themes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/florm/latest/actions/list-public-design-themes?${params}`, {
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
      "body": {},
      "guid": "string",
      "isDefault": true,
      "isPublic": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | object | Theme style definition. |
| `guid` | string | GUID of the design theme. |
| `isDefault` | boolean | Whether the theme is marked as default. |
| `isPublic` | boolean | Whether the theme is public. |
| `name` | string | Theme name. |

## Native endpoint

Through the native Florm API, this operation is `GET /v1/design-themes/` (base URL `https://api.florm.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-public-design-themes.md) for the provider-specific parameters and requirements.

