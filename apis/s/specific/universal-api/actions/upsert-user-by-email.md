# Specific: Upsert User By Email

Creates or updates a user in Specific by email.

```
PUT https://connect.mindcloud.co/v1/universal/specific/latest/actions/upsert-user-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Specific `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/specific/latest/actions/upsert-user-by-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.email": "ava@example.com",
  "variables.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/specific/latest/actions/upsert-user-by-email', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.email": "ava@example.com",
    "variables.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.email` | string | yes |  |
| `variables.id` | string | no |  |
| `variables.name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {
        "id": "string",
        "name": "Ava Chen"
      },
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "visitorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company.id` | string |  |
| `company.name` | string |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `visitorId` | string |  |

## Native endpoint

Through the native Specific API, this operation is `POST` (base URL `https://public-api.specific.app/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-user-by-email.md) for the provider-specific parameters and requirements.

