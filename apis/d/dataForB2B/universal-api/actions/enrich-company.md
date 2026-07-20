# DataForB2B: Enrich Company

Retrieves enriched company data from DataForB2B.

```
GET https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/enrich-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForB2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/enrich-company?connectionId=$CONNECTION_ID&companyIdentifier=google.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyIdentifier": "google.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/enrich-company?${params}`, {
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
| `companyIdentifier` | string | yes | Company name, domain, LinkedIn URL, or company ID to enrich. Default: `google.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object |  |

## Native endpoint

Through the native DataForB2B API, this operation is `POST /enrich/company` (base URL `https://api.dataforb2b.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-company.md) for the provider-specific parameters and requirements.

