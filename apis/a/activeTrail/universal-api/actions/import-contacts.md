# ActiveTrail: Import Contacts

Imports contacts into a group in ActiveTrail.

```
POST https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/import-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveTrail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/import-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts[]": [
    {}
  ],
  "group": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/import-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts[]": [{}],
    "group": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contacts[]` | array<object> | yes | Contacts to import. Limited to 1000. |
| `contacts[].anniversary` | date | no |  |
| `contacts[].birthday` | date | no |  |
| `contacts[].city` | string | no |  |
| `contacts[].email` | string | no |  |
| `contacts[].first_name` | string | no |  |
| `contacts[].last_name` | string | no |  |
| `contacts[].phone1` | string | no |  |
| `contacts[].phone2` | string | no |  |
| `contacts[].sms` | string | no |  |
| `group` | number | yes | Group id. Required. |
| `mailingList` | number | no | Mailing list id. Delete it if you don't have mailing lists on your account. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActiveTrail API returns.

## Native endpoint

Through the native ActiveTrail API, this operation is `POST /contacts/Import` (base URL `https://webapi.mymarketing.co.il/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-contacts.md) for the provider-specific parameters and requirements.

