# Adyntel: List LinkedIn Ads

Retrieves LinkedIn ads from Adyntel by company domain.

```
GET https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/list-linked-in-ads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adyntel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/list-linked-in-ads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/list-linked-in-ads?${params}`, {
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
| `linkedinPageId` | string | no | LinkedIn page ID. Example: `15564`. |
| `companyDomain` | string | no | Company website. Example: `shopify.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ads": [
        {}
      ],
      "continuation_token": "string",
      "is_last_page": true,
      "page_id": "string",
      "total_ads": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ads` | array<object> |  |
| `continuation_token` | string |  |
| `is_last_page` | boolean |  |
| `page_id` | string |  |
| `total_ads` | number |  |

## Native endpoint

Through the native Adyntel API, this operation is `POST /linkedin` (base URL `https://api.adyntel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-linked-in-ads.md) for the provider-specific parameters and requirements.

