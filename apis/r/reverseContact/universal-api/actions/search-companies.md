# Reverse Contact: Search Companies



```
GET https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/search-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reverse Contact `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/search-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/search-companies?${params}`, {
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
| `companyDomain` | string | no | Filter by company website domain, such as openai.com. |
| `companyName` | string | no | Filter by company name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyUpdateDate": "2026-05-07T12:00:00.000Z",
      "employeeCountRange": {
        "end": 1,
        "start": 1
      },
      "employeesCount": 1,
      "followersCount": 1,
      "industry": "string",
      "linkedinId": "https://example.com",
      "linkedinUrl": "https://example.com",
      "location": {
        "city": "string",
        "country": "string"
      },
      "name": "Ava Chen",
      "publicId": "string",
      "tagline": "string",
      "websiteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyUpdateDate` | date |  |
| `employeeCountRange.end` | number |  |
| `employeeCountRange.start` | number |  |
| `employeesCount` | number |  |
| `followersCount` | number |  |
| `industry` | string |  |
| `linkedinId` | string |  |
| `linkedinUrl` | string |  |
| `location.city` | string |  |
| `location.country` | string |  |
| `name` | string |  |
| `publicId` | string |  |
| `tagline` | string |  |
| `websiteUrl` | string |  |

## Native endpoint

Through the native Reverse Contact API, this operation is `POST /v2/search/companies` (base URL `https://api.reversecontact.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-companies.md) for the provider-specific parameters and requirements.

