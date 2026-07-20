# ProdPad: List Companies

Retrieves companies from ProdPad.

```
GET https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProdPad `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/list-companies?${params}`, {
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
| `country` | string | no | Filter companies by ISO Alpha-2 country code. |
| `companySize` | string | no | Filter companies by company size. |
| `value` | string | no | Filter companies by value. |
| `city` | string | no | Filter companies by city. |
| `tags` | string | no | Filter companies by one or more tag IDs or UUIDs. Accepts multiple values in one string, delimited by `,`. |
| `name` | string | no | Filter companies by company name or partial name. |
| `externalId` | string | no | Filter companies by an external ID. |
| `externalUrl` | string | no | Filter companies by an external URL. |
| `contacts` | boolean | no | Include contacts associated with each company. |
| `feedbacks` | boolean | no | Include feedback associated with each company's contacts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companies": [
        {
          "city": "string",
          "country": "string",
          "created_at": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "name": "Ava Chen",
          "size": "string",
          "updated_at": "2026-05-07T12:00:00.000Z",
          "value": "string"
        }
      ],
      "company_count": 1,
      "include": {
        "contacts": true,
        "feedbacks": true
      },
      "page": 1,
      "size": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companies[].city` | string |  |
| `companies[].country` | string |  |
| `companies[].created_at` | date |  |
| `companies[].id` | string |  |
| `companies[].name` | string |  |
| `companies[].size` | string |  |
| `companies[].updated_at` | date |  |
| `companies[].value` | string |  |
| `company_count` | number |  |
| `include.contacts` | boolean |  |
| `include.feedbacks` | boolean |  |
| `page` | number |  |
| `size` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native ProdPad API, this operation is `GET /companies` (base URL `https://api.prodpad.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

