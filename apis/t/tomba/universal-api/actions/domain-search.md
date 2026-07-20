# Tomba: Domain Search

Finds contacts in Tomba by domain.

```
GET https://connect.mindcloud.co/v1/universal/tomba/latest/actions/domain-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tomba `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tomba/latest/actions/domain-search?connectionId=$CONNECTION_ID&limit=25&offset=0&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tomba/latest/actions/domain-search?${params}`, {
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
| `domain` | string | yes | Domain to search for company contacts. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company` | string | no | Company name to search when a domain is not available. |
| `page` | number | no | Page number to retrieve. |
| `limit` | string | no | Maximum number of results to return. |
| `country` | string | no | Two-letter country code to narrow the search. |
| `department` | string | no | Department filter for returned contacts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emails": [
        {
          "email": "ava@example.com",
          "full_name": "ava@example.com",
          "position": "ava@example.com",
          "score": 1,
          "verification": {
            "status": "ava@example.com"
          }
        }
      ],
      "organization": {
        "company_size": "string",
        "location": {
          "country": "string"
        },
        "organization": "string",
        "website_url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emails[].email` | string |  |
| `emails[].full_name` | string |  |
| `emails[].position` | string |  |
| `emails[].score` | number |  |
| `emails[].verification.status` | string |  |
| `organization.company_size` | string |  |
| `organization.location.country` | string |  |
| `organization.organization` | string |  |
| `organization.website_url` | string |  |

## Native endpoint

Through the native Tomba API, this operation is `GET /domain-search` (base URL `https://api.tomba.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/domain-search.md) for the provider-specific parameters and requirements.

