# CRM Messaging: Delete Contact

Deletes an existing contact from CRM Messaging.

```
DELETE https://connect.mindcloud.co/v1/universal/cRMMessaging/latest/actions/delete-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CRM Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cRMMessaging/latest/actions/delete-contact?connectionId=$CONNECTION_ID&phone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cRMMessaging/latest/actions/delete-contact?${params}`, {
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
| `phone` | string | yes | Contact phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native CRM Messaging API, this operation is `POST /index.php/Api/deleteContact` (base URL `https://app.crm-messaging.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact.md) for the provider-specific parameters and requirements.

