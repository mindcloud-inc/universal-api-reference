# Adyntel: List Facebook and Instagram Ads

Retrieves Facebook and Instagram ads from Adyntel by company or page.

```
GET https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/list-facebook-and-instagram-ads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adyntel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/list-facebook-and-instagram-ads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/list-facebook-and-instagram-ads?${params}`, {
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
| `facebookUrl` | string | no | Facebook page URL starting with https://. Example: `https://facebook.com/shopify`. |
| `companyDomain` | string | no | Company website. Example: `shopify.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active_status": "string",
      "continuation_token": "string",
      "count_landing_pages": 1,
      "country_code": "string",
      "is_result_complete": true,
      "media_types": "string",
      "number_of_ads": 1,
      "page_id": "string",
      "platform": [
        "string"
      ],
      "results": [
        {}
      ],
      "sort_data": "string",
      "unique_landing_pages": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active_status` | string |  |
| `continuation_token` | string |  |
| `count_landing_pages` | number |  |
| `country_code` | string |  |
| `is_result_complete` | boolean |  |
| `media_types` | string |  |
| `number_of_ads` | number |  |
| `page_id` | string |  |
| `platform` | array<string> |  |
| `results` | array<object> |  |
| `sort_data` | string |  |
| `unique_landing_pages` | array<string> |  |

## Native endpoint

Through the native Adyntel API, this operation is `POST /facebook` (base URL `https://api.adyntel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-facebook-and-instagram-ads.md) for the provider-specific parameters and requirements.

