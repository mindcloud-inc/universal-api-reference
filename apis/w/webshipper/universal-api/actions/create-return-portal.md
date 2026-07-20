# Webshipper: Create Return Portal

Creates a return portal in Webshipper.

```
POST https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-return-portal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-return-portal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.attributes.name": "Ava Chen",
  "data.relationships.orderChannel.data.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-return-portal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.attributes.name": "Ava Chen",
    "data.relationships.orderChannel.data.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.attributes.name` | string | yes | Name of the return portal. |
| `data.relationships.orderChannel.data.id` | string | yes | The order channel ID to connect to the portal. |
| `data.relationships.slipTemplate.data.id` | string | no | Optional slip template ID. |
| `data.relationships.mailTemplate.data.id` | string | no | Optional mail template ID. |
| `data.relationships.returnAddress.data.id` | string | no | Optional return address ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowed_days_since_dispatch": "string",
      "custom_style": "string",
      "email_address_resource_options": [
        "ava@example.com"
      ],
      "email_address_source": "ava@example.com",
      "finished_stripe_setup": "string",
      "force_single_page": true,
      "id": "string",
      "locale": "string",
      "logo": "string",
      "mail_templateId": "string",
      "name": "Ava Chen",
      "new_confirmation_mail_template": "string",
      "new_mail_template": "string",
      "optional_return_cause": true,
      "order_channel_id": 1,
      "order_channel_logo": "string",
      "send_immediately": true,
      "shipping_methods": [
        "string"
      ],
      "static_notice_email": "ava@example.com",
      "translations": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowed_days_since_dispatch` | string |  |
| `custom_style` | string |  |
| `email_address_resource_options` | array<string> |  |
| `email_address_source` | string |  |
| `finished_stripe_setup` | string |  |
| `force_single_page` | boolean |  |
| `id` | string |  |
| `locale` | string |  |
| `logo` | string |  |
| `mail_templateId` | string |  |
| `name` | string |  |
| `new_confirmation_mail_template` | string |  |
| `new_mail_template` | string |  |
| `optional_return_cause` | boolean |  |
| `order_channel_id` | number |  |
| `order_channel_logo` | string |  |
| `send_immediately` | boolean |  |
| `shipping_methods` | array<string> |  |
| `static_notice_email` | string |  |
| `translations` | array<string> |  |
| `type` | string |  |

## Native endpoint

Through the native Webshipper API, this operation is `POST /return_portals` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-return-portal.md) for the provider-specific parameters and requirements.

