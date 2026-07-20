# FindyMail: Enrich Company

Retrieves company enrichment data from FindyMail.

```
GET https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/enrich-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FindyMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/enrich-company?connectionId=$CONNECTION_ID&domain=stripe.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "stripe.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/enrich-company?${params}`, {
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
| `domain` | string | yes | Company domain to enrich, for example stripe.com. Example: `stripe.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "company_size": "string",
      "country": "string",
      "description": "string",
      "domain": "string",
      "industry": "string",
      "linkedin_url": "https://example.com",
      "name": "Ava Chen",
      "region": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string | Company city. |
| `company_size` | string | Company size range. |
| `country` | string | Company country. |
| `description` | string | Company description. |
| `domain` | string | Company domain. |
| `industry` | string | Company industry. |
| `linkedin_url` | string | Company LinkedIn URL. |
| `name` | string | Company name. |
| `region` | string | Company region. |

## Native endpoint

Through the native FindyMail API, this operation is `POST /api/search/company` (base URL `https://app.findymail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-company.md) for the provider-specific parameters and requirements.

