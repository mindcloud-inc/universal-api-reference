# HappyFox: Update Contact Group Members

Updates contacts in a HappyFox contact group.

```
PUT https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/update-contact-group-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/update-contact-group-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactGroupId": "string",
  "contacts[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/update-contact-group-members', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactGroupId": "string",
    "contacts[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactGroupId` | string | yes | HappyFox contact group ID. |
| `contacts[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Result details for the membership update, including the contact ID and access setting. |
| `success` | boolean | Whether the requested membership change succeeded for this contact. |

## Native endpoint

Through the native HappyFox API, this operation is `POST /contact_group/:contact_group_id/update_contacts/` (base URL `https://{{credentials.accountDomain}}/api/1.1/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-group-members.md) for the provider-specific parameters and requirements.

