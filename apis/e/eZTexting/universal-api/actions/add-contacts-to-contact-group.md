# EZ Texting: Add Contacts to Contact Group

Adds contacts to a contact group in EZ Texting.

```
PUT https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/add-contacts-to-contact-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EZ Texting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/add-contacts-to-contact-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "phoneNumbers[]": "(737) 337-8315"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/add-contacts-to-contact-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "phoneNumbers[]": "(737) 337-8315"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Contact group ID |
| `phoneNumbers[]` | array<string> | yes | Phone numbers to add Example: `(737) 337-8315`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value0": "string",
      "value1": "string",
      "value10": "string",
      "value2": "string",
      "value3": "string",
      "value4": "string",
      "value5": "string",
      "value6": "string",
      "value7": "string",
      "value8": "string",
      "value9": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value0` | string |  |
| `value1` | string |  |
| `value10` | string |  |
| `value2` | string |  |
| `value3` | string |  |
| `value4` | string |  |
| `value5` | string |  |
| `value6` | string |  |
| `value7` | string |  |
| `value8` | string |  |
| `value9` | string |  |

## Native endpoint

Through the native EZ Texting API, this operation is `POST /contact-groups/:id/contacts` (base URL `https://a.eztexting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contacts-to-contact-group.md) for the provider-specific parameters and requirements.

