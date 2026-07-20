# Testlify: List Candidates

Retrieves candidates from Testlify with optional filters and pagination.

```
GET https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-candidates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testlify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-candidates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-candidates?${params}`, {
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
| `query` | string | no | Search query string. |
| `assessmentId` | string | no | Assessment identifier. |
| `email` | string | no | Filter by candidate email. |
| `candidateStatus` | string | no | Filter by candidate status. |
| `sortBy` | string | no | Column name to sort by. |
| `sortOrder` | string | no | Sort order. |
| `limit` | number | no | Number of items to return. |
| `skip` | number | no | Number of items to skip. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "candidateId": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "lastSeenAt": "string",
      "totalAssessment": 1,
      "totalTest": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `candidateId` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `lastSeenAt` | string |  |
| `totalAssessment` | number |  |
| `totalTest` | number |  |

## Native endpoint

Through the native Testlify API, this operation is `GET /v1/candidate` (base URL `https://api.testlify.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-candidates.md) for the provider-specific parameters and requirements.

