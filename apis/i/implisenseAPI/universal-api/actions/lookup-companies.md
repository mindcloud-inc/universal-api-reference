# Implisense: Lookup Companies

Finds companies in Implisense API by known attributes.

```
GET https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/lookup-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Implisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/lookup-companies?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/lookup-companies?${params}`, {
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
| `query` | string | yes | Known company data to match, such as a company name or city. |
| `name` | string | no | Official company name. |
| `city` | string | no | City of the company headquarters. |
| `active` | boolean | no | Return only companies that are still active. |
| `size` | number | no | Maximum number of results to return, up to 10. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "city": "string",
      "id": "string",
      "name": "Ava Chen",
      "profile": "string",
      "street": "string",
      "url": "https://example.com",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `city` | string |  |
| `id` | string |  |
| `name` | string |  |
| `profile` | string |  |
| `street` | string |  |
| `url` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native Implisense API, this operation is `POST /lookup` (base URL `https://german-company-data.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-companies.md) for the provider-specific parameters and requirements.

