# Channels: Add Contact Alternative MSISDN

Creates an alternative contact phone number in Channels.

```
POST https://connect.mindcloud.co/v1/universal/channels/latest/actions/add-contact-alternative-msisdn
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/channels/latest/actions/add-contact-alternative-msisdn" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": 1,
  "msisdn": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/channels/latest/actions/add-contact-alternative-msisdn', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": 1,
    "msisdn": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | number | yes | Contact ID to add an alternative MSISDN to. |
| `msisdn` | string | yes | Phone number to add as an alternative MSISDN. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "msisdn": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `msisdn` | string |  |

## Native endpoint

Through the native Channels API, this operation is `POST /api/v1/contacts/{contactId}/alternative-msisdns` (base URL `https://api.channels.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact-alternative-msisdn.md) for the provider-specific parameters and requirements.

