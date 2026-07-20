# HappyFox: Update Contact Group

Updates an existing contact group in HappyFox.

```
PUT https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/update-contact-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/update-contact-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactGroupId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/update-contact-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactGroupId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactGroupId` | string | yes | HappyFox contact group ID. |
| `description` | string | no | Updated contact group description. |
| `taggedDomains` | string | no | Updated domains tagged to the group. |

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

Through the native HappyFox API, this operation is `POST /contact_group/:contact_group_id/` (base URL `https://{{credentials.accountDomain}}/api/1.1/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-group.md) for the provider-specific parameters and requirements.

