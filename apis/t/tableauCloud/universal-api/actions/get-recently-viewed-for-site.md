# Tableau Cloud: Get Recently Viewed for Site

Retrieves recently viewed content from Tableau Cloud.

```
GET https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/get-recently-viewed-for-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tableau Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/get-recently-viewed-for-site?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/get-recently-viewed-for-site?${params}`, {
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
      "contentUrl": "https://example.com",
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "string",
      "viewUrlName": "https://example.com",
      "webpageUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentUrl` | string | Content URL. |
| `createdAt` | string | Creation timestamp. |
| `id` | string | Recently viewed item ID. |
| `name` | string | Recently viewed item name. |
| `updatedAt` | string | Last update timestamp. |
| `viewUrlName` | string | View URL name when the item is a view. |
| `webpageUrl` | string | Web URL when available. |

## Native endpoint

Through the native Tableau Cloud API, this operation is `GET /sites/site-id/content/recent` (base URL `https://us-east-1.online.tableau.com/api/3.28`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recently-viewed-for-site.md) for the provider-specific parameters and requirements.

