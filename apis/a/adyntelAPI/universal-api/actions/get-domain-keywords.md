# Adyntel: Get Domain Keywords

Retrieves paid and organic keywords for a domain in Adyntel.

```
GET https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/get-domain-keywords
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adyntel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/get-domain-keywords?connectionId=$CONNECTION_ID&companyDomain=clay.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyDomain": "clay.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/get-domain-keywords?${params}`, {
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
| `companyDomain` | string | yes | Company website without www or http. Example: `clay.com`. |
| `language` | string | no | Language for keyword results. Default: `English`. |
| `limit` | number | no | Number of results to return. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "organic": {},
      "organic_percentages": {},
      "paid": {},
      "paid_percentages": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organic` | object |  |
| `organic_percentages` | object |  |
| `paid` | object |  |
| `paid_percentages` | object |  |

## Native endpoint

Through the native Adyntel API, this operation is `POST /domain-keywords` (base URL `https://api.adyntel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-keywords.md) for the provider-specific parameters and requirements.

