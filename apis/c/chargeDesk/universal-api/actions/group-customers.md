# ChargeDesk: Group Customers

Retrieves grouped customers from ChargeDesk.

```
GET https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/group-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/group-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/group-customers?${params}`, {
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
| `query` | string | no | Text to find matching customers and charges by name, email, username, phone, or last 4 card digits. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customers": [
        {}
      ],
      "match": {
        "matches": "string",
        "param": "string",
        "score": 1
      },
      "search": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customers` | array<object> |  |
| `match` | object |  |
| `match.matches` | string |  |
| `match.param` | string |  |
| `match.score` | number |  |
| `search` | string |  |

## Native endpoint

Through the native ChargeDesk API, this operation is `GET /customers/grouped` (base URL `https://api.chargedesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/group-customers.md) for the provider-specific parameters and requirements.

