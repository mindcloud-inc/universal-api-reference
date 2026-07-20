# Teamgate: Get Company

Retrieves a company from Teamgate.

```
GET https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamgate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/get-company?connectionId=$CONNECTION_ID&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/get-company?${params}`, {
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
| `companyId` | string | yes | Company ID to retrieve. |

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

Through the native Teamgate API, this operation is `GET /companies/{{companyId}}` (base URL `https://api.teamgate.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

