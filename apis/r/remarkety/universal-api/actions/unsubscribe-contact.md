# Remarkety: Unsubscribe Contact



```
PUT https://connect.mindcloud.co/v1/universal/remarkety/latest/actions/unsubscribe-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Remarkety `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/remarkety/latest/actions/unsubscribe-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/remarkety/latest/actions/unsubscribe-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no |  |
| `sms_phone_number_e164` | string | no |  |
| `reason` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "info": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `info` | object | Echoed contact identifier fields returned after unsubscribe. |
| `status` | string | Provider status string returned by Remarkety. |

## Native endpoint

Through the native Remarkety API, this operation is `POST /api/v1/stores/{{credentials.storeId}}/contacts/unsubscribe` (base URL `https://app.remarkety.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-contact.md) for the provider-specific parameters and requirements.

