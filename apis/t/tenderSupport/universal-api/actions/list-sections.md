# Tender Support: List Sections

Retrieves support sections from Tender Support.

```
GET https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/list-sections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tender Support `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/list-sections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/list-sections?${params}`, {
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
      "beta": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "faqsCount": 1,
      "faqsHref": "string",
      "href": "string",
      "htmlHref": "string",
      "important": true,
      "permalink": "https://example.com",
      "redirectionId": 1,
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `beta` | boolean |  |
| `createdAt` | date |  |
| `faqsCount` | number |  |
| `faqsHref` | string |  |
| `href` | string |  |
| `htmlHref` | string |  |
| `important` | boolean |  |
| `permalink` | string |  |
| `redirectionId` | number |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Tender Support API, this operation is `GET /sections` (base URL `https://api.tenderapp.com/help`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sections.md) for the provider-specific parameters and requirements.

