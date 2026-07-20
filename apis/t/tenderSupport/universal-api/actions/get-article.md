# Tender Support: Get Article

Retrieves a knowledge base article from Tender Support.

```
GET https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/get-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tender Support `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/get-article?connectionId=$CONNECTION_ID&faqId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "faqId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/get-article?${params}`, {
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
| `faqId` | number | yes | The Tender knowledge-base article ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "beta": true,
      "body": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "formattedBody": "string",
      "href": "string",
      "htmlHref": "string",
      "important": true,
      "keywords": "string",
      "permalink": "https://example.com",
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "ratingNegative": 1,
      "ratingPositive": 1,
      "sectionHref": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `beta` | boolean |  |
| `body` | string |  |
| `createdAt` | date |  |
| `formattedBody` | string |  |
| `href` | string |  |
| `htmlHref` | string |  |
| `important` | boolean |  |
| `keywords` | string |  |
| `permalink` | string |  |
| `publishedAt` | date |  |
| `ratingNegative` | number |  |
| `ratingPositive` | number |  |
| `sectionHref` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Tender Support API, this operation is `GET /faqs/:faqId` (base URL `https://api.tenderapp.com/help`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-article.md) for the provider-specific parameters and requirements.

