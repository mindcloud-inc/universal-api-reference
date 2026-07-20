# Storyblok: Get Current Space

Retrieves the current space from Storyblok.

```
GET https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/get-current-space
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storyblok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/get-current-space?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/get-current-space?${params}`, {
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
      "space": {
        "domain": "string",
        "id": 1,
        "languageCodes": [
          "string"
        ],
        "name": "Ava Chen",
        "version": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `space` | object | The current Storyblok space. |
| `space.domain` | string | The Storyblok space domain. |
| `space.id` | number | The Storyblok space ID. |
| `space.languageCodes` | array<string> | Configured language codes for the space. |
| `space.name` | string | The Storyblok space name. |
| `space.version` | number | The current cache version for the space. |

## Native endpoint

Through the native Storyblok API, this operation is `GET /spaces/me` (base URL `https://api.storyblok.com/v2/cdn`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-space.md) for the provider-specific parameters and requirements.

