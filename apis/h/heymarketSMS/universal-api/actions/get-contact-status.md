# Heymarket SMS: Get Contact Status



```
GET https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-contact-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heymarket SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-contact-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-contact-status?${params}`, {
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
| `id` | number | no | Heymarket contact id to check. |
| `phone` | string | no | Contact phone number to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blocked": true,
      "id": 1,
      "phone": "string",
      "unsubscribed": true,
      "unsubscribed_admin": true,
      "unsubscribed_contact": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocked` | boolean |  |
| `id` | number |  |
| `phone` | string |  |
| `unsubscribed` | boolean |  |
| `unsubscribed_admin` | boolean |  |
| `unsubscribed_contact` | boolean |  |

## Native endpoint

Through the native Heymarket SMS API, this operation is `POST /v1/contact/status` (base URL `https://api.heymarket.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-status.md) for the provider-specific parameters and requirements.

