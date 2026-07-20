# Clockodo: Create Service

Creates a service in your Clockodo account.

```
POST https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/create-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockodo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/create-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/create-service', {
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
| `active` | boolean | no |  |
| `name` | string | yes |  |
| `note` | string | no |  |
| `number` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "billableDefault": true,
      "id": "string",
      "name": "Ava Chen",
      "note": "string",
      "number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `billableDefault` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `note` | string |  |
| `number` | string |  |

## Native endpoint

Through the native Clockodo API, this operation is `POST /services` (base URL `https://my.clockodo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-service.md) for the provider-specific parameters and requirements.

