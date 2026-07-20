# Aspire: Update Property Contacts



```
PUT https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-property-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-property-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "propertyid": 1,
  "contactid": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-property-contacts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "propertyid": 1,
    "contactid": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `propertyid` | list<number> | yes |  |
| `contactid` | list<number> | yes |  |
| `billingcontact` | boolean | no |  |
| `emailinvoicecontact` | boolean | no |  |
| `primarycontact` | boolean | no |  |
| `emailnotificationscontact` | boolean | no |  |
| `smsnotificationscontact` | boolean | no |  |
| `viewinaspiremobile` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `PUT PropertyContacts` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-property-contacts.md) for the provider-specific parameters and requirements.

