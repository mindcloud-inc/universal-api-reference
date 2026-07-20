# Less Annoying CRM: Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Less Annoying CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | The contact or company Id to update. |
| `assignedTo` | string | no | User Id that should own the record. |
| `name` | string | no | Updated full name of the contact or company. |
| `companyName` | string | no | Updated company name. |
| `jobTitle` | string | no | Updated job title for the contact. |
| `backgroundInfo` | string | no | Updated background information. |
| `birthday` | date | no | Updated birthday for the contact. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Less Annoying CRM API returns.

## Native endpoint

Through the native Less Annoying CRM API, this operation is `POST /` (base URL `https://api.lessannoyingcrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

