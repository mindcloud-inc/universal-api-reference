# Constant Contact: Update Contact Tag

Renames a contact tag in Constant Contact.

```
PUT https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/update-contact-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/update-contact-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tagId": "cc4f2295-76bd-44f3-a07f-1ea4be3f1473",
  "name": "VIP Customers"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/update-contact-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tagId": "cc4f2295-76bd-44f3-a07f-1ea4be3f1473",
    "name": "VIP Customers"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tagId` | string | yes | UUID of the tag to update. Example: `cc4f2295-76bd-44f3-a07f-1ea4be3f1473`. |
| `name` | string | yes | Updated tag name. Example: `VIP Customers`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactsCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "tagId": "string",
      "tagSource": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactsCount` | number |  |
| `createdAt` | date |  |
| `name` | string |  |
| `tagId` | string |  |
| `tagSource` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Constant Contact API, this operation is `PUT /contact_tags/:tag_id` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-tag.md) for the provider-specific parameters and requirements.

