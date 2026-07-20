# folk: List Companies

Retrieves a list of companies from folk.

```
GET https://connect.mindcloud.co/v1/universal/folk/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a folk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/folk/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/folk/latest/actions/list-companies?${params}`, {
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
      "addresses": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "customFieldValues": {},
      "description": "string",
      "emails": [
        "ava@example.com"
      ],
      "employeeRange": "string",
      "foundationYear": 1,
      "fundingRaised": 1,
      "groups": [
        {}
      ],
      "id": "string",
      "industry": "string",
      "lastFundingDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "phones": [
        "string"
      ],
      "urls": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<string> |  |
| `createdAt` | date |  |
| `createdBy` | object |  |
| `customFieldValues` | object |  |
| `description` | string |  |
| `emails` | array<string> |  |
| `employeeRange` | string |  |
| `foundationYear` | number |  |
| `fundingRaised` | number |  |
| `groups` | array<object> |  |
| `id` | string |  |
| `industry` | string |  |
| `lastFundingDate` | date |  |
| `name` | string |  |
| `phones` | array<string> |  |
| `urls` | array<string> |  |

## Native endpoint

Through the native folk API, this operation is `GET /v1/companies` (base URL `https://api.folk.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

