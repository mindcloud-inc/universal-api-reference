# Calibre: List Sites

Retrieves all available sites from Calibre.

```
GET https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-sites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-sites?${params}`, {
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
      "organisation": {
        "sitesList": {
          "nodes": [
            {
              "canonicalUrl": "https://example.com",
              "name": "Ava Chen",
              "slug": "string"
            }
          ],
          "totalCount": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organisation.sitesList.nodes[].canonicalUrl` | string |  |
| `organisation.sitesList.nodes[].name` | string |  |
| `organisation.sitesList.nodes[].slug` | string |  |
| `organisation.sitesList.totalCount` | number |  |

## Native endpoint

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sites.md) for the provider-specific parameters and requirements.

