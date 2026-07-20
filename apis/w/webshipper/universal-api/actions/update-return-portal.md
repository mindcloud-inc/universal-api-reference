# Webshipper: Update Return Portal

Updates a return portal in Webshipper.

```
PUT https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/update-return-portal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/update-return-portal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "data.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/update-return-portal', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "data.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The return portal ID. |
| `data.id` | string | yes | Repeat the ID value for the JSON:API request body. |
| `data.attributes.name` | string | no | Updated portal name. |

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

Through the native Webshipper API, this operation is `PATCH /return_portals/:id` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-return-portal.md) for the provider-specific parameters and requirements.

