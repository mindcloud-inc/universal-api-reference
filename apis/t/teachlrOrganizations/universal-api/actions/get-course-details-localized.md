# Teachlr Organizations: Get Course Details Localized



```
GET https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/get-course-details-localized
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teachlr Organizations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/get-course-details-localized?connectionId=$CONNECTION_ID&slug=marketing-digital&lang=es" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "marketing-digital",
  "lang": "es"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/get-course-details-localized?${params}`, {
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
| `slug` | string | yes | Slug of the course to retrieve. Default: `marketing-digital`. |
| `lang` | string | yes | ISO 639-1 language code to localize category and subcategory labels. Default: `es`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasCoupons": true,
      "headline": "string",
      "id": 1,
      "language": "string",
      "numChapters": 1,
      "price": "string",
      "slug": "string",
      "status": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasCoupons` | boolean |  |
| `headline` | string |  |
| `id` | number |  |
| `language` | string |  |
| `numChapters` | number |  |
| `price` | string |  |
| `slug` | string |  |
| `status` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Teachlr Organizations API, this operation is `GET /courses-online/:slug` (base URL `https://api.teachlr.com/mindcloudteachlr337933/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-course-details-localized.md) for the provider-specific parameters and requirements.

