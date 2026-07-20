# Bulldog-WP: Get contact

Retrieves a contact from Bulldog-WP.

```
GET https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-device-contact-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulldog-WP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-device-contact-details?connectionId=$CONNECTION_ID&contactWid=string&deviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactWid": "string",
  "deviceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-device-contact-details?${params}`, {
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
| `contactWid` | string | yes | WhatsApp contact ID or phone number. |
| `deviceId` | string | yes | WhatsApp number device ID from Bulldog WP. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "broadcastId": "string",
      "channelId": "string",
      "chat": {},
      "countryCode": 1,
      "displayName": "Ava Chen",
      "formattedName": "Ava Chen",
      "formattedShortName": "Ava Chen",
      "groupId": "string",
      "name": "Ava Chen",
      "phone": "string",
      "shortName": "Ava Chen",
      "wid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `broadcastId` | string |  |
| `channelId` | string |  |
| `chat` | object |  |
| `countryCode` | number |  |
| `displayName` | string |  |
| `formattedName` | string |  |
| `formattedShortName` | string |  |
| `groupId` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `shortName` | string |  |
| `wid` | string |  |

## Native endpoint

Through the native Bulldog-WP API, this operation is `GET /chat/{deviceId}/contacts/{contactWid}` (base URL `https://api.bulldog-wp.co.il/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-device-contact-details.md) for the provider-specific parameters and requirements.

