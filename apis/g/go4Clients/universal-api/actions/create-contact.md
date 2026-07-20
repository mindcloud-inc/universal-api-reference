# Go4Clients: Create Contact

Creates a new contact in Go4Clients.

```
POST https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mobileNumber": "573001234500"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mobileNumber": "573001234500"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mobileNumber` | string | yes | Contact phone number. Example: `573001234500`. |
| `name` | string | no | Custom field value for name. Example: `Stage 3 Contact`. |
| `sex` | string | no | Custom field value for sex. Example: `F`. |
| `weight` | string | no | Custom field value for weight. Example: `95`. |
| `height` | string | no | Custom field value for height. Example: `1.82`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "height": "string",
      "lastUpdate": "2026-05-07T12:00:00.000Z",
      "mobileNumber": "string",
      "name": "Ava Chen",
      "sex": "string",
      "source": "string",
      "weight": "string",
      "whiteLabelId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `createdOn` | date |  |
| `height` | string |  |
| `lastUpdate` | date |  |
| `mobileNumber` | string |  |
| `name` | string |  |
| `sex` | string |  |
| `source` | string |  |
| `weight` | string |  |
| `whiteLabelId` | string |  |

## Native endpoint

Through the native Go4Clients API, this operation is `POST /api/groupscontacts/contacts/v1.0` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

