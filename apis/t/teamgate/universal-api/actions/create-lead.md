# Teamgate: Create Lead

Creates a new lead in Teamgate.

```
POST https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamgate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/create-lead', {
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
| `name` | string | yes | Lead name. |
| `companyName` | string | no | Company name when linking or creating lead company context. |
| `companyId` | string | no | Existing company ID to link to the lead. |
| `jobTitle` | string | no | Lead job title. |
| `statusId` | string | no | Lead status ID. |
| `starred` | string | no | Whether the lead is starred. Use Teamgate values like yes or no. |
| `source` | string | no | Lead source name. |
| `industry` | string | no | Lead industry name. |
| `tags` | string | no | Lead tags. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ownerId` | string | no | Owner user ID. |
| `ownerUsername` | string | no | Owner username. |
| `sourceDescription` | string | no | Lead source description. |
| `industryDescription` | string | no | Lead industry description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "company": {},
      "created": {},
      "emails": [
        {}
      ],
      "id": 1,
      "industry": {},
      "isDeleted": "string",
      "name": "Ava Chen",
      "owner": {},
      "phones": [
        {}
      ],
      "picture": {},
      "score": {},
      "source": {},
      "starred": "string",
      "status": {},
      "updated": {},
      "urls": [
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
| `addresses` | array<object> |  |
| `company` | object |  |
| `created` | object |  |
| `emails` | array<object> |  |
| `id` | number |  |
| `industry` | object |  |
| `isDeleted` | string |  |
| `name` | string |  |
| `owner` | object |  |
| `phones` | array<object> |  |
| `picture` | object |  |
| `score` | object |  |
| `source` | object |  |
| `starred` | string |  |
| `status` | object |  |
| `updated` | object |  |
| `urls` | array<object> |  |

## Native endpoint

Through the native Teamgate API, this operation is `POST /leads` (base URL `https://api.teamgate.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

