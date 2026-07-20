# WhatsApp Number Validator: Validate WhatsApp Number

Retrieves WhatsApp number validation details from WhatsApp Number Validator.

```
GET https://connect.mindcloud.co/v1/universal/whatsAppNumberValidator/latest/actions/validate-whats-app-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsApp Number Validator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsAppNumberValidator/latest/actions/validate-whats-app-number?connectionId=$CONNECTION_ID&number=14083742784" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "number": "14083742784"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whatsAppNumberValidator/latest/actions/validate-whats-app-number?${params}`, {
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
| `number` | string | yes | Phone number with country code and no leading plus sign. Example: `14083742784`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WhatsApp Number Validator API returns.

## Native endpoint

Through the native WhatsApp Number Validator API, this operation is `GET number+check` (base URL `https://zylalabs.com/api/9470/whatsapp+number+validator+api/21752`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-whats-app-number.md) for the provider-specific parameters and requirements.

