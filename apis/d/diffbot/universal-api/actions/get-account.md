# Diffbot: Get Account

Retrieves Diffbot account details and usage information.

```
GET https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Diffbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/get-account?${params}`, {
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
      "created": "string",
      "email": "ava@example.com",
      "name": "Ava Chen",
      "plan": "string",
      "planCredits": 1,
      "planStart": "string",
      "status": "string",
      "token": "string",
      "usage": [
        {
          "credits": 1,
          "date": "string",
          "entities": 1,
          "extractions": 1,
          "facets": 1,
          "nlp": 1,
          "proxies": 1,
          "refresh": 1,
          "subtitles": 1,
          "videos": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string | Account creation date. |
| `email` | string | Account email address. |
| `name` | string | Account owner name. |
| `plan` | string | Current Diffbot plan name. |
| `planCredits` | number | Remaining plan credits for the current Diffbot account. |
| `planStart` | string | Account plan start date. |
| `status` | string | Account status. |
| `token` | string | Current token returned by Diffbot. |
| `usage` | array<object> | Recent daily Diffbot usage records. |
| `usage[].credits` | number | Credits consumed that day. |
| `usage[].date` | string | Usage day. |
| `usage[].entities` | number | Entities queried that day. |
| `usage[].extractions` | number | Extractions run that day. |
| `usage[].facets` | number | Facet operations that day. |
| `usage[].nlp` | number | Natural language requests that day. |
| `usage[].proxies` | number | Proxy usage that day. |
| `usage[].refresh` | number | Refresh operations that day. |
| `usage[].subtitles` | number | Subtitle operations that day. |
| `usage[].videos` | number | Video requests that day. |

## Native endpoint

Through the native Diffbot API, this operation is `GET /v4/account` (base URL `https://api.diffbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

