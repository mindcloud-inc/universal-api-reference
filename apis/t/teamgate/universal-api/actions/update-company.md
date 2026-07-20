# Teamgate: Update Company

Updates a company in Teamgate.

```
PUT https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/update-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamgate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/update-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/update-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | yes | Company ID to update. |
| `industry` | string | no | Updated company industry name. |
| `name` | string | no | Updated company name. |
| `ownerId` | string | no | Updated owner user ID. |
| `source` | string | no | Updated company source name. |
| `starred` | string | no | Whether the company is starred. Use Teamgate values like yes or no. |
| `tags` | string | no | Updated company tags. |

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

Through the native Teamgate API, this operation is `PUT /companies/{{companyId}}` (base URL `https://api.teamgate.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company.md) for the provider-specific parameters and requirements.

