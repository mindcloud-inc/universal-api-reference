# Trove: Get Bulk Transaction Result

Retrieves the result of a bulk enrichment request from Trove.

```
GET https://connect.mindcloud.co/v1/universal/trove/latest/actions/get-bulk-transaction-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trove/latest/actions/get-bulk-transaction-result?connectionId=$CONNECTION_ID&bulkRequestToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bulkRequestToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trove/latest/actions/get-bulk-transaction-result?${params}`, {
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
| `bulkRequestToken` | string | yes | The bulk request ID returned by Enrich Bulk Transactions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        "string"
      ],
      "domain": "string",
      "facebook_url": "https://example.com",
      "founded": "string",
      "handle": "string",
      "hq_city": "string",
      "hq_country_code": "string",
      "hq_state": "string",
      "hq_state_code": "string",
      "id": "string",
      "industry": "string",
      "linkedin_url": "https://example.com",
      "name": "Ava Chen",
      "query": {},
      "size": "string",
      "summary": "string",
      "twitter_url": "https://example.com",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | array<string> | Business categories associated with the matched company. |
| `domain` | string | Company domain matched to the transaction. |
| `facebook_url` | string | Official Facebook URL. |
| `founded` | string | Company founding date or year. |
| `handle` | string | Trove company handle. |
| `hq_city` | string | Headquarters city. |
| `hq_country_code` | string | Country code returned by Trove. Docs say ISO alpha-2, but live responses currently return values like USA. |
| `hq_state` | string | Headquarters state. |
| `hq_state_code` | string | USPS state code for US companies. |
| `id` | string | Provider row identifier. Trove docs describe this as the submitted user_id, but live bulk responses currently return null. |
| `industry` | string | Industry classification. |
| `linkedin_url` | string | Official LinkedIn URL. |
| `name` | string | Company name. |
| `query` | object | Original transaction request data echoed by Trove, including description, amount, date, and user_id. |
| `size` | string | Approximate employee headcount band. |
| `summary` | string | Short company summary. |
| `twitter_url` | string | Official X/Twitter URL. |
| `type` | string | Company type such as Public Company or Privately Held. |

## Native endpoint

Through the native Trove API, this operation is `GET /transactions/bulk/:requestId` (base URL `https://trove.headline.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-transaction-result.md) for the provider-specific parameters and requirements.

