# Hunter: Create Lead



```
POST https://connect.mindcloud.co/v1/universal/hunter/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hunter/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `position` | string | no |  |
| `company` | string | no |  |
| `companyIndustry` | string | no |  |
| `companySize` | string | no |  |
| `confidenceScore` | number | no |  |
| `website` | string | no |  |
| `countryCode` | string | no |  |
| `linkedinUrl` | string | no |  |
| `phoneNumber` | string | no |  |
| `twitter` | string | no |  |
| `notes` | string | no |  |
| `source` | string | no |  |
| `leadsListId` | string | no |  |
| `leadsListIds` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "companyIndustry": "string",
      "companySize": "string",
      "confidenceScore": 1,
      "countryCode": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastActivityAt": "string",
      "lastContactedAt": "string",
      "lastName": "Chen",
      "leadsList": {},
      "linkedinUrl": "https://example.com",
      "notes": "string",
      "phoneNumber": "string",
      "position": "string",
      "sendingStatus": "string",
      "source": "string",
      "syncStatus": "string",
      "twitter": "string",
      "verification": {},
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `companyIndustry` | string |  |
| `companySize` | string |  |
| `confidenceScore` | number |  |
| `countryCode` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastActivityAt` | string |  |
| `lastContactedAt` | string |  |
| `lastName` | string |  |
| `leadsList` | object |  |
| `linkedinUrl` | string |  |
| `notes` | string |  |
| `phoneNumber` | string |  |
| `position` | string |  |
| `sendingStatus` | string |  |
| `source` | string |  |
| `syncStatus` | string |  |
| `twitter` | string |  |
| `verification` | object |  |
| `website` | string |  |

## Native endpoint

Through the native Hunter API, this operation is `POST /leads` (base URL `https://api.hunter.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

