# Hunter: List Leads



```
GET https://connect.mindcloud.co/v1/universal/hunter/latest/actions/list-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/list-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hunter/latest/actions/list-leads?${params}`, {
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
| `leadsListId` | string | no |  |
| `email` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `position` | string | no |  |
| `company` | string | no |  |
| `industry` | string | no |  |
| `website` | string | no |  |
| `countryCode` | string | no |  |
| `companySize` | string | no |  |
| `source` | string | no |  |
| `twitter` | string | no |  |
| `linkedinUrl` | string | no |  |
| `phoneNumber` | string | no |  |
| `syncStatus` | string | no |  |
| `sendingStatus` | string | no |  |
| `verificationStatus` | string | no |  |
| `lastActivityAt` | string | no |  |
| `lastContactedAt` | string | no |  |
| `query` | string | no |  |
| `limit` | number | no |  |
| `offset` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "leads": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `leads` | array<object> |  |

## Native endpoint

Through the native Hunter API, this operation is `GET /leads` (base URL `https://api.hunter.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-leads.md) for the provider-specific parameters and requirements.

