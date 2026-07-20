# Clio Manage: Create Person Contact

Creates a new person contact in Clio Manage.

```
POST https://connect.mindcloud.co/v1/universal/clio/latest/actions/create-person-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clio Manage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clio/latest/actions/create-person-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.first_name": "Ava"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clio/latest/actions/create-person-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.first_name": "Ava"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.first_name` | string | yes |  |
| `data.last_name` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "id": 1,
      "initials": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `id` | number |  |
| `initials` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Clio Manage API, this operation is `POST /contacts.json` (base URL `https://app.clio.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person-contact.md) for the provider-specific parameters and requirements.

