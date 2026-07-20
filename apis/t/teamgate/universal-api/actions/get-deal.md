# Teamgate: Get Deal

Retrieves a deal from Teamgate.

```
GET https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/get-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamgate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/get-deal?connectionId=$CONNECTION_ID&dealId=79" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dealId": "79"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/get-deal?${params}`, {
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
| `dealId` | string | yes | Deal ID to retrieve. Example: `79`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost": {},
      "created": {},
      "estimatedClosureDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isDeleted": "string",
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
| `cost` | object |  |
| `created` | object |  |
| `estimatedClosureDate` | date |  |
| `id` | number |  |
| `isDeleted` | string |  |
| `name` | string |  |
| `owner` | object |  |
| `pipeline` | object |  |
| `price` | object |  |
| `source` | object |  |
| `stage` | object |  |
| `starred` | string |  |
| `status` | object |  |

## Native endpoint

Through the native Teamgate API, this operation is `GET /deals/:deal_id` (base URL `https://api.teamgate.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deal.md) for the provider-specific parameters and requirements.

