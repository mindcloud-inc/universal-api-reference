# Onfleet: Find Recipient

Finds a recipient in Onfleet by name or phone.

```
GET https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/find-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onfleet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/find-recipient?connectionId=$CONNECTION_ID&lookupType=string&lookupValue=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lookupType": "string",
  "lookupValue": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/find-recipient?${params}`, {
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
| `lookupType` | string | yes | Which recipient property to search by. Use name or phone. |
| `lookupValue` | string | yes | The exact recipient name or phone number to look up. |
| `skipPhoneNumberValidation` | boolean | no | When true, bypasses phone validation for recipients created without validation. |

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

Through the native Onfleet API, this operation is `GET /recipients/:lookupType/:lookupValue` (base URL `https://onfleet.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-recipient.md) for the provider-specific parameters and requirements.

