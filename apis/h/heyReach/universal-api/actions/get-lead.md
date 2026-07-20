# Hey Reach: Get Lead

Retrieves a lead from Hey Reach by LinkedIn profile URL.

```
GET https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hey Reach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-lead?connectionId=$CONNECTION_ID&profileUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-lead?${params}`, {
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
| `profileUrl` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "about": "string",
      "companyName": "Ava Chen",
      "companyUrl": "https://example.com",
      "connections": 1,
      "education": "string",
      "emailAddress": "ava@example.com",
      "emailEnrichments": [
        "ava@example.com"
      ],
      "enrichedEmailAddress": "ava@example.com",
      "experiences": "string",
      "firstName": "Ava",
      "followers": 1,
      "fullName": "Ava Chen",
      "headline": "string",
      "imageUrl": "https://example.com",
      "industry": "string",
      "lastName": "Chen",
      "linkedinId": "https://example.com",
      "location": "string",
      "position": "string",
      "profileUrl": "https://example.com",
      "summary": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `about` | string |  |
| `companyName` | string |  |
| `companyUrl` | string |  |
| `connections` | number |  |
| `education` | string |  |
| `emailAddress` | string |  |
| `emailEnrichments` | array<string> |  |
| `enrichedEmailAddress` | string |  |
| `experiences` | string |  |
| `firstName` | string |  |
| `followers` | number |  |
| `fullName` | string |  |
| `headline` | string |  |
| `imageUrl` | string |  |
| `industry` | string |  |
| `lastName` | string |  |
| `linkedinId` | string |  |
| `location` | string |  |
| `position` | string |  |
| `profileUrl` | string |  |
| `summary` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Hey Reach API, this operation is `POST /api/public/lead/GetLead` (base URL `https://api.heyreach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead.md) for the provider-specific parameters and requirements.

