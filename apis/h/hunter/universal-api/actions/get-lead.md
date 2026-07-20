# Hunter: Get Lead



```
GET https://connect.mindcloud.co/v1/universal/hunter/latest/actions/get-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/get-lead?connectionId=$CONNECTION_ID&leadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hunter/latest/actions/get-lead?${params}`, {
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
| `leadId` | string | yes | Identifier of the lead. |

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

Through the native Hunter API, this operation is `GET /leads/:leadId` (base URL `https://api.hunter.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead.md) for the provider-specific parameters and requirements.

