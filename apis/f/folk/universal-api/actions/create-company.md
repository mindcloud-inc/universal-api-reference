# folk: Create Company

Creates a new company in folk.

```
POST https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a folk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | An optional description for the company. |
| `name` | string | yes | The company name. |

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

Through the native folk API, this operation is `POST /v1/companies` (base URL `https://api.folk.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

