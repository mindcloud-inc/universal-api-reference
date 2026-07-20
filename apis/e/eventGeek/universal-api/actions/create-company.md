# EventGeek: Create Company

Creates a new company in EventGeek.

```
POST https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EventGeek `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud delete company disposable 2026-04-21 16:20"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud delete company disposable 2026-04-21 16:20"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Company name. Default: `MindCloud delete company disposable 2026-04-21 16:20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "city": "string",
      "country": "string",
      "custom_fields": {},
      "id": "string",
      "name": "Ava Chen",
      "phone": "string",
      "state": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `country` | string |  |
| `custom_fields` | object |  |
| `id` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `state` | string |  |
| `website` | string |  |

## Native endpoint

Through the native EventGeek API, this operation is `POST /companies` (base URL `https://app.circa.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

