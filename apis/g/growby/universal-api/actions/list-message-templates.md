# Growby: List Message Templates

Retrieves message templates from Growby.

```
GET https://connect.mindcloud.co/v1/universal/growby/latest/actions/list-message-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Growby `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/growby/latest/actions/list-message-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growby/latest/actions/list-message-templates?${params}`, {
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
| `accessToken` | string | no | Meta Cloud API access token with WhatsApp permissions. |
| `email` | string | no | Email address associated with the WABA setup. |
| `phoneNumberId` | string | no | Meta phone number ID for the linked WhatsApp sender. |
| `whatsappBusinessAccountId` | string | no | WhatsApp Business Account ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Growby API returns.

## Native endpoint

Through the native Growby API, this operation is `GET /v1/messages_templates` (base URL `https://api.growby.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-message-templates.md) for the provider-specific parameters and requirements.

