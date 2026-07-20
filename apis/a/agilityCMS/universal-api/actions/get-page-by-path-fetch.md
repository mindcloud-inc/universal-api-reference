# Agility CMS: Get Page By Path (Fetch)

Retrieves a published page by path from Agility CMS.

```
GET https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-page-by-path-fetch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agility CMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-page-by-path-fetch?connectionId=$CONNECTION_ID&path=%2Fhome" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "path": "/home"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-page-by-path-fetch?${params}`, {
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
| `path` | string | yes | The page path to resolve, for example /home or /blog. Example: `/home`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "page": {
        "pageID": 1,
        "properties": {},
        "title": "string",
        "zones": {}
      },
      "sitemapNode": {
        "pageID": 1,
        "path": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page` | object |  |
| `page.pageID` | number |  |
| `page.properties` | object |  |
| `page.title` | string |  |
| `page.zones` | object |  |
| `sitemapNode` | object |  |
| `sitemapNode.pageID` | number |  |
| `sitemapNode.path` | string |  |
| `sitemapNode.title` | string |  |

## Native endpoint

Through the native Agility CMS API, this operation is `GET /:guid/fetch/:locale/page/:channel` (base URL `https://api.aglty.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-by-path-fetch.md) for the provider-specific parameters and requirements.

