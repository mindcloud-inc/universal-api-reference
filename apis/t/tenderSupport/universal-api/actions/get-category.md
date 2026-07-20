# Tender Support: Get Category

Retrieves a category from Tender Support.

```
GET https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/get-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tender Support `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/get-category?connectionId=$CONNECTION_ID&categoryId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "categoryId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/get-category?${params}`, {
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
| `categoryId` | number | yes | The Tender category ID. |

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

Through the native Tender Support API, this operation is `GET /categories/:categoryId` (base URL `https://api.tenderapp.com/help`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-category.md) for the provider-specific parameters and requirements.

