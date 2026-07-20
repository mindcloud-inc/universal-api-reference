# Agility CMS: List Categories (Preview)

Retrieves preview categories from Agility CMS.

```
GET https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/list-categories-preview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agility CMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/list-categories-preview?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/list-categories-preview?${params}`, {
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
          "contentID": 1,
          "fields": {},
          "properties": {},
          "seo": {}
        }
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `items[].contentID` | number |  |
| `items[].fields` | object |  |
| `items[].properties` | object |  |
| `items[].seo` | object |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Agility CMS API, this operation is `GET /:guid/preview/:locale/list/categories` (base URL `https://api.aglty.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-categories-preview.md) for the provider-specific parameters and requirements.

