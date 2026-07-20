# LeadIQ: Search Company



```
GET https://connect.mindcloud.co/v1/universal/leadIQ/latest/actions/search-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadIQ/latest/actions/search-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadIQ/latest/actions/search-company?${params}`, {
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
| `id` | string | no | Search by the LeadIQ company identifier. |
| `name` | string | no | Search by company name. |
| `domain` | string | no | Search by company domain, for example leadiq.com. |
| `linkedinId` | string | no | Search by the LinkedIn company ID. |
| `linkedinUrl` | string | no | Search by the LinkedIn company URL. |
| `strict` | boolean | no | When true, require a stricter match against the identifiers you provide. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "description": "string",
      "domain": "string",
      "id": "string",
      "industry": "string",
      "isExcluded": true,
      "linkedinId": "https://example.com",
      "linkedinUrl": "https://example.com",
      "logoUrl": "https://example.com",
      "name": "Ava Chen",
      "numberOfEmployees": 1,
      "updatedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `description` | string |  |
| `domain` | string |  |
| `id` | string |  |
| `industry` | string |  |
| `isExcluded` | boolean |  |
| `linkedinId` | string |  |
| `linkedinUrl` | string |  |
| `logoUrl` | string |  |
| `name` | string |  |
| `numberOfEmployees` | number |  |
| `updatedDate` | date |  |

## Native endpoint

Through the native LeadIQ API, this operation is `POST graphql` (base URL `https://api.leadiq.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-company.md) for the provider-specific parameters and requirements.

