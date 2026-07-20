# OptiMonk: List Leads

Retrieves leads from OptiMonk.

```
GET https://connect.mindcloud.co/v1/universal/optiMonk/latest/actions/list-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OptiMonk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optiMonk/latest/actions/list-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optiMonk/latest/actions/list-leads?${params}`, {
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
| `interval` | string | no | Predefined reporting interval. |
| `from` | string | no | Start date or datetime for a custom interval. |
| `to` | string | no | End date or datetime for a custom interval. |
| `page` | number | no | Pagination index. Starts at 1. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": {},
      "createdAt": "string",
      "customFields": {},
      "email": "ava@example.com",
      "errors": [
        {}
      ],
      "firstName": "Ava",
      "lastName": "Chen",
      "phone": "string",
      "syncStatus": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | object |  |
| `createdAt` | string |  |
| `customFields` | object |  |
| `email` | string |  |
| `errors` | array<object> |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `phone` | string |  |
| `syncStatus` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native OptiMonk API, this operation is `GET /leads/` (base URL `https://api.optimonk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-leads.md) for the provider-specific parameters and requirements.

