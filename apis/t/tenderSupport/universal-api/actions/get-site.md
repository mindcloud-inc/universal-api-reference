# Tender Support: Get Site

Retrieves site details from Tender Support.

```
GET https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/get-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tender Support `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/get-site?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/get-site?${params}`, {
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
      "categoriesHref": "string",
      "discussionsHref": "string",
      "faqsHref": "string",
      "href": "string",
      "htmlHref": "string",
      "name": "Ava Chen",
      "permalink": "https://example.com",
      "profileHref": "string",
      "sectionsHref": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoriesHref` | string |  |
| `discussionsHref` | string |  |
| `faqsHref` | string |  |
| `href` | string |  |
| `htmlHref` | string |  |
| `name` | string |  |
| `permalink` | string |  |
| `profileHref` | string |  |
| `sectionsHref` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Tender Support API, this operation is `GET /` (base URL `https://api.tenderapp.com/help`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site.md) for the provider-specific parameters and requirements.

