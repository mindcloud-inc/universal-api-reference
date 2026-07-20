# LaGrowthMachine: Search Leads

Finds leads in LaGrowthMachine.

```
GET https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/search-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaGrowthMachine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/search-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/search-leads?${params}`, {
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
| `companyName` | string | no | Filter by company name. |
| `companyUrl` | string | no | Filter by company website URL. |
| `email` | string | no | Filter by lead email. |
| `firstname` | string | no | Filter by lead first name. |
| `lastname` | string | no | Filter by lead last name. |
| `leadId` | string | no | Filter by lead ID. |
| `linkedinUrl` | string | no | Filter by lead LinkedIn profile URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lead": {
        "audiences": [
          [
            "string"
          ]
        ],
        "companyName": "Ava Chen",
        "companyUrl": "https://example.com",
        "createdAt": 1,
        "firstname": "Ava",
        "id": "string",
        "lastname": "Chen",
        "linkedinUrl": "https://example.com",
        "modifiedAt": 1,
        "persoEmail": "ava@example.com",
        "proEmail": "ava@example.com"
      },
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lead.audiences[]` | array<string> | Audience identifiers attached to the lead. |
| `lead.companyName` | string | Lead company name. |
| `lead.companyUrl` | string | Lead company URL. |
| `lead.createdAt` | number | Lead creation timestamp. |
| `lead.firstname` | string | Lead first name. |
| `lead.id` | string | Lead identifier. |
| `lead.lastname` | string | Lead last name. |
| `lead.linkedinUrl` | string | Lead LinkedIn profile URL. |
| `lead.modifiedAt` | number | Lead last update timestamp. |
| `lead.persoEmail` | string | Lead personal email. |
| `lead.proEmail` | string | Lead professional email. |
| `statusCode` | number | Provider status code returned by the lead search endpoint. |

## Native endpoint

Through the native LaGrowthMachine API, this operation is `GET /leads/search` (base URL `https://apiv2.lagrowthmachine.com/flow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-leads.md) for the provider-specific parameters and requirements.

