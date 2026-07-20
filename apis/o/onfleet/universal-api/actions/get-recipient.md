# Onfleet: Get Recipient

Retrieves a recipient from Onfleet.

```
GET https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onfleet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-recipient?connectionId=$CONNECTION_ID&recipientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recipientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-recipient?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recipientId` | string | yes | The Onfleet recipient ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "notes": "string",
      "phone": "string",
      "skipSMSNotifications": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `skipSMSNotifications` | boolean |  |

## Native endpoint

Through the native Onfleet API, this operation is `GET /recipients/:recipientId` (base URL `https://onfleet.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recipient.md) for the provider-specific parameters and requirements.

