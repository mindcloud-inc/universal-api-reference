# EZ Texting: Create Contact Group

Creates a contact group in EZ Texting.

```
POST https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/create-contact-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EZ Texting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/create-contact-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/create-contact-group', {
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
| `groupIds[]` | array<string> | no | Nested contact groups to include |
| `name` | string | yes | Contact group name |
| `note` | string | no | Contact group note |
| `phoneNumbers[]` | array<string> | no | Phone numbers to include in the group Example: `(737) 337-8315`. |
| `strictValidation` | boolean | no | Require strict validation for provided contacts |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native EZ Texting API, this operation is `POST /contact-groups` (base URL `https://a.eztexting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-group.md) for the provider-specific parameters and requirements.

