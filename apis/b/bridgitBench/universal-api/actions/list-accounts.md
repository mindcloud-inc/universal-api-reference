# Bridgit Bench: List Accounts



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-accounts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "logoUrl": "https://example.com",
      "status": "string",
      "numProjects": 1,
      "numPeople": 1,
      "numMembers": 1,
      "expiryDate": "string",
      "totalPeopleAttachmentBytes": 1,
      "useMetricUnits": true,
      "organizationId": "string",
      "isDemo": true,
      "companyType": "string",
      "marketSegment": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `logoUrl` | string |  |
| `status` | string |  |
| `numProjects` | number |  |
| `numPeople` | number |  |
| `numMembers` | number |  |
| `expiryDate` | string |  |
| `totalPeopleAttachmentBytes` | number |  |
| `useMetricUnits` | boolean |  |
| `organizationId` | string |  |
| `isDemo` | boolean |  |
| `companyType` | string |  |
| `marketSegment` | string |  |

## Native endpoint

Through the native Bridgit Bench API, this operation is `GET /rp/api/v1/Accounts` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.

