# Teamgate: Create Company

Creates a new company in Teamgate.

```
POST https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamgate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/create-company', {
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
| `name` | string | yes | Company name. |
| `jobTitle` | string | no | Primary company contact job title. |
| `starred` | string | no | Whether the company is starred. Use Teamgate values like yes or no. |
| `tags` | string | no | Company tags. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `personId` | string | no | Existing person ID to associate with the company. |
| `customerStatusId` | string | no | Customer status ID. |
| `prospectStatusId` | string | no | Prospect status ID. |
| `ownerId` | string | no | Owner user ID. |
| `sourceId` | string | no | Company source ID. |
| `industryId` | string | no | Company industry ID. |
| `code` | string | no | Company registration code. |
| `vatCode` | string | no | Company VAT code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "converted": {},
      "created": {},
      "customerStatus": {},
      "emails": [
        {}
      ],
      "id": 1,
      "industry": {},
      "isDeleted": "string",
      "name": "Ava Chen",
      "owner": {},
      "person": {},
      "phones": [
        {}
      ],
      "picture": {},
      "prospectStatus": {},
      "source": {},
      "starred": "string",
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
| `converted` | object |  |
| `created` | object |  |
| `customerStatus` | object |  |
| `emails` | array<object> |  |
| `id` | number |  |
| `industry` | object |  |
| `isDeleted` | string |  |
| `name` | string |  |
| `owner` | object |  |
| `person` | object |  |
| `phones` | array<object> |  |
| `picture` | object |  |
| `prospectStatus` | object |  |
| `source` | object |  |
| `starred` | string |  |
| `updated` | object |  |
| `urls` | array<object> |  |

## Native endpoint

Through the native Teamgate API, this operation is `POST /companies` (base URL `https://api.teamgate.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

