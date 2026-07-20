# HappyFox: Create Contact Group

Creates a new contact group in HappyFox.

```
POST https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/create-contact-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/create-contact-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/create-contact-group', {
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
| `name` | string | yes | Contact group name. |
| `description` | string | no | Optional contact group description. |
| `taggedDomains` | string | no | Optional domains to tag to the group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "taggedDomains": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Contact group description. |
| `id` | number | HappyFox contact group ID. |
| `name` | string | Contact group display name. |
| `taggedDomains` | string | Comma-delimited domains auto-associated with the group. |

## Native endpoint

Through the native HappyFox API, this operation is `POST /contact_groups/` (base URL `https://{{credentials.accountDomain}}/api/1.1/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-group.md) for the provider-specific parameters and requirements.

