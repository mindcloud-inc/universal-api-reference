# Go4Clients: Update Contact

Updates an existing contact in Go4Clients.

```
PUT https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "_id": "string",
  "mobileNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "_id": "string",
    "mobileNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `_id` | string | yes | ID of the contact to update. |
| `mobileNumber` | string | yes | Contact phone number in international format. |
| `name` | string | no | Updated contact name. |
| `sex` | string | no | Updated contact sex field. |
| `weight` | string | no | Updated contact weight field. |
| `height` | string | no | Updated contact height field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdOn": "string",
      "height": "string",
      "lastUpdate": "string",
      "mobileNumber": "string",
      "name": "Ava Chen",
      "sex": "string",
      "source": "string",
      "weight": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `createdOn` | string |  |
| `height` | string |  |
| `lastUpdate` | string |  |
| `mobileNumber` | string |  |
| `name` | string |  |
| `sex` | string |  |
| `source` | string |  |
| `weight` | string |  |

## Native endpoint

Through the native Go4Clients API, this operation is `PUT /api/groupscontacts/contacts/v1.0` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

