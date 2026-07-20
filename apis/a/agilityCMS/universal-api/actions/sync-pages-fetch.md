# Agility CMS: Sync Pages (Fetch)

Retrieves published page sync data from Agility CMS.

```
GET https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/sync-pages-fetch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agility CMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/sync-pages-fetch?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/sync-pages-fetch?${params}`, {
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
      "items": [
        {
          "pageID": 1,
          "properties": {},
          "title": "string",
          "zones": {}
        }
      ],
      "syncToken": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `items[].pageID` | number |  |
| `items[].properties` | object |  |
| `items[].title` | string |  |
| `items[].zones` | object |  |
| `syncToken` | number |  |

## Native endpoint

Through the native Agility CMS API, this operation is `GET /:guid/fetch/:locale/sync/pages` (base URL `https://api.aglty.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sync-pages-fetch.md) for the provider-specific parameters and requirements.

