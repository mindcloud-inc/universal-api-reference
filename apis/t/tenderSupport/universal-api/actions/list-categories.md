# Tender Support: List Categories

Retrieves support categories from Tender Support.

```
GET https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/list-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tender Support `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/list-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/list-categories?${params}`, {
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
      "discussionsHref": "string",
      "href": "string",
      "htmlHref": "string",
      "lastUpdatedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "permalink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `discussionsHref` | string |  |
| `href` | string |  |
| `htmlHref` | string |  |
| `lastUpdatedAt` | date |  |
| `name` | string |  |
| `permalink` | string |  |

## Native endpoint

Through the native Tender Support API, this operation is `GET /categories` (base URL `https://api.tenderapp.com/help`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-categories.md) for the provider-specific parameters and requirements.

