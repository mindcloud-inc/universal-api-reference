# DitLead: Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DitLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "attributes": {},
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "attributes": {},
    "contactId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attributes` | object | yes | Contact attributes to update (for example first_name, company, phone). |
| `contactId` | string | yes | Public ID of the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "_id": "string",
        "addedVia": "string",
        "attributes": {},
        "campaignsParticipated": [
          "string"
        ],
        "emails": [
          {}
        ],
        "list": [
          "string"
        ],
        "publicId": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data._id` | string |  |
| `data.addedVia` | string |  |
| `data.attributes` | object |  |
| `data.campaignsParticipated` | array<string> |  |
| `data.emails` | array<object> |  |
| `data.list` | array<string> |  |
| `data.publicId` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native DitLead API, this operation is `PUT /v1/contact/{contactId}` (base URL `https://api.ditlead.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

