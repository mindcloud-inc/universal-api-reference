# Teamgate: List Person Deals

Retrieves deals for a person in Teamgate.

```
GET https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-person-deals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamgate `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-person-deals?connectionId=$CONNECTION_ID&limit=25&offset=0&personId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "personId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-person-deals?${params}`, {
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
| `personId` | string | yes | Person ID whose deals should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allBuyers": [
        {}
      ],
      "buyer": {},
      "cost": {},
      "created": {},
      "estimatedClosureDate": "string",
      "id": 1,
      "isDeleted": "string",
      "loss": [
        {}
      ],
      "name": "Ava Chen",
      "owner": {},
      "pipeline": {},
      "price": {},
      "source": {},
      "stage": {},
      "starred": "string",
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allBuyers` | array<object> |  |
| `buyer` | object |  |
| `cost` | object |  |
| `created` | object |  |
| `estimatedClosureDate` | string |  |
| `id` | number |  |
| `isDeleted` | string |  |
| `loss` | array<object> |  |
| `name` | string |  |
| `owner` | object |  |
| `pipeline` | object |  |
| `price` | object |  |
| `source` | object |  |
| `stage` | object |  |
| `starred` | string |  |
| `status` | object |  |

## Native endpoint

Through the native Teamgate API, this operation is `GET /people/{{personId}}/deals` (base URL `https://api.teamgate.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-person-deals.md) for the provider-specific parameters and requirements.

