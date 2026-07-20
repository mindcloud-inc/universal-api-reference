# Quentn: Retrieve Contact



```
GET https://connect.mindcloud.co/v1/universal/quentn/latest/actions/retrieve-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quentn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quentn/latest/actions/retrieve-contact?connectionId=$CONNECTION_ID&contact_id=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact_id": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quentn/latest/actions/retrieve-contact?${params}`, {
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
| `contact_id` | number | yes | The numeric Quentn contact ID to retrieve. This must be an existing contact id, not an email address. Example: `123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "familyName": "Ava Chen",
      "firstName": "Ava",
      "id": "string",
      "mail": "string",
      "mailStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `familyName` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `mail` | string |  |
| `mailStatus` | string |  |

## Native endpoint

Through the native Quentn API, this operation is `GET /contact/:contact_id` (base URL `https://tbg6y3.us-1.quentn.com/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-contact.md) for the provider-specific parameters and requirements.

