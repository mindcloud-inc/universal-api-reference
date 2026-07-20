# LeadIQ: Flat Advanced Search



```
GET https://connect.mindcloud.co/v1/universal/leadIQ/latest/actions/flat-advanced-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadIQ/latest/actions/flat-advanced-search?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadIQ/latest/actions/flat-advanced-search?${params}`, {
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
| `companyFilter` | object | no | CompanyFilter object. Common keys include domains, names, linkedinIds, industries, sizes, locations, and revenue filters. |
| `contactFilter` | object | no | ContactFilter object. Common keys include names, titles, linkedinIds, seniorities, roles, locations, updatedAt, newHireFrom, and newPromotionFrom. |
| `limit` | number | no | Maximum number of contacts to return. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyExcludedFilter` | object | no | Optional CompanyFilter object for companies to exclude from the search. |
| `contactExcludedFilter` | object | no | Optional ContactFilter object for contacts to exclude from the search. |
| `sortContactsBy[]` | array<string> | no | Optional array of contact sort values such as UpdatedAtDesc, NameAsc, RoleAsc, or SeniorityDesc. |
| `skip` | number | no | Number of matching contacts to skip before returning results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "company": {
        "domain": "string",
        "employeeCount": 1,
        "id": "string",
        "industry": "string",
        "linkedinId": "https://example.com",
        "name": "Ava Chen"
      },
      "country": "string",
      "id": "string",
      "linkedinId": "https://example.com",
      "linkedinUrl": "https://example.com",
      "name": "Ava Chen",
      "role": "string",
      "seniority": "string",
      "state": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "verifiedWorkEmails": [
        [
          "ava@example.com"
        ]
      ],
      "workEmails": [
        [
          "ava@example.com"
        ]
      ],
      "workPhones": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `company.domain` | string |  |
| `company.employeeCount` | number |  |
| `company.id` | string |  |
| `company.industry` | string |  |
| `company.linkedinId` | string |  |
| `company.name` | string |  |
| `country` | string |  |
| `id` | string |  |
| `linkedinId` | string |  |
| `linkedinUrl` | string |  |
| `name` | string |  |
| `role` | string |  |
| `seniority` | string |  |
| `state` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `verifiedWorkEmails[]` | array<string> |  |
| `workEmails[]` | array<string> |  |
| `workPhones[]` | array<string> |  |

## Native endpoint

Through the native LeadIQ API, this operation is `POST graphql` (base URL `https://api.leadiq.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/flat-advanced-search.md) for the provider-specific parameters and requirements.

