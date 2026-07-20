# Agility CMS: Get Sitemap Flat (Preview)

Retrieves the preview sitemap as a flat list from Agility CMS.

```
GET https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-sitemap-flat-preview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agility CMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-sitemap-flat-preview?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-sitemap-flat-preview?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agility CMS API returns.

## Native endpoint

Through the native Agility CMS API, this operation is `GET /:guid/preview/:locale/sitemap/flat/:channelName` (base URL `https://api.aglty.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sitemap-flat-preview.md) for the provider-specific parameters and requirements.

