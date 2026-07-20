# Agility CMS: Get Sitemap Nested (Preview)

Retrieves the preview sitemap in nested format from Agility CMS.

```
GET https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-sitemap-nested-preview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agility CMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-sitemap-nested-preview?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-sitemap-nested-preview?${params}`, {
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
      "": [
        {
          "children": [
            {}
          ],
          "pageID": 1,
          "path": "string",
          "title": "string"
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
| `[]` | array<object> |  |
| `[].children` | array<object> |  |
| `[].pageID` | number |  |
| `[].path` | string |  |
| `[].title` | string |  |

## Native endpoint

Through the native Agility CMS API, this operation is `GET /:guid/preview/:locale/sitemap/nested/:channelName` (base URL `https://api.aglty.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sitemap-nested-preview.md) for the provider-specific parameters and requirements.

