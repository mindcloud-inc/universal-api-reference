# ChatDaddy: Check Contact Exists

Checks whether a contact exists in ChatDaddy.

```
GET https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/check-contact-exists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatDaddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/check-contact-exists?connectionId=$CONNECTION_ID&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/check-contact-exists?${params}`, {
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
| `type` | string | yes | Platform type to check, for example a WhatsApp user lookup. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exists": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exists` | boolean | Whether the contact exists for the requested platform type. |

## Native endpoint

Through the native ChatDaddy API, this operation is `GET /contacts/exists` (base URL `https://api.chatdaddy.tech/im`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-contact-exists.md) for the provider-specific parameters and requirements.

