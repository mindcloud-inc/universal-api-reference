# Agility CMS: List Content Items (Fetch)

Retrieves published content items from Agility CMS.

```
GET https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/list-content-items-fetch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agility CMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/list-content-items-fetch?connectionId=$CONNECTION_ID&limit=25&offset=0&referenceName=posts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "referenceName": "posts"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/list-content-items-fetch?${params}`, {
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
| `referenceName` | string | yes | The lowercase content list reference name, for example posts or categories. Default: `posts`. |

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

Through the native Agility CMS API, this operation is `GET /:guid/fetch/:locale/list/:referenceName` (base URL `https://api.aglty.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-content-items-fetch.md) for the provider-specific parameters and requirements.

