# Makeplans: Create Person

Creates a new person in Makeplans.

```
POST https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/create-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeplans `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/create-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/create-person', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Person email. |
| `name` | string | no | Person name. |
| `phoneNumber` | string | no | Person phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blocked": true,
      "email": "ava@example.com",
      "external_id": "string",
      "id": 1,
      "name": "Ava Chen",
      "phone_number": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocked` | boolean |  |
| `email` | string |  |
| `external_id` | string |  |
| `id` | number |  |
| `name` | string |  |
| `phone_number` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Makeplans API, this operation is `POST /people` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person.md) for the provider-specific parameters and requirements.

