# Magileads: Update Contact In List

Updates a contact in a Magileads contact list.

```
PUT https://connect.mindcloud.co/v1/universal/magileads/latest/actions/update-contact-in-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Magileads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/magileads/latest/actions/update-contact-in-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact_list_id": 1,
  "contact_id": 1,
  "properties[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/magileads/latest/actions/update-contact-in-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact_list_id": 1,
    "contact_id": 1,
    "properties[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact_list_id` | number | yes | The contact list ID. |
| `contact_id` | number | yes | The contact ID. |
| `properties[]` | array<object> | yes | The contact properties to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts_added": 1,
      "contacts_deleted": 1,
      "contacts_ignored": 1,
      "contacts_updated": 1,
      "contacts_with_ignored_fields": 1,
      "state": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts_added` | number |  |
| `contacts_deleted` | number |  |
| `contacts_ignored` | number |  |
| `contacts_updated` | number |  |
| `contacts_with_ignored_fields` | number |  |
| `state` | boolean |  |

## Native endpoint

Through the native Magileads API, this operation is `PUT /contact-lists/:contact_list_id/contacts/:contact_id` (base URL `https://app.api-magileads.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-in-list.md) for the provider-specific parameters and requirements.

