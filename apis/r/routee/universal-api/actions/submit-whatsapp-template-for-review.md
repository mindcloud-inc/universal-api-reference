# Routee: Submit Whatsapp Template for review

Submits a WhatsApp template for review in Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/submit-whatsapp-template-for-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/submit-whatsapp-template-for-review" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "whatsappAccountId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/submit-whatsapp-template-for-review', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "whatsappAccountId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `whatsappAccountId` | string | yes | WhatsApp account id |
| `templateName` | string | no | The name of the Template. Max 512 ASCII char set |
| `templateCategory` | string | no | Category of the template. Fixed set as per documentation. |
| `localizations` | string | no | Localizations of the template |
| `language` | string | no | Supported language codes can be found at https://developers.facebook.com/docs/whatsapp/business-management-api/message-templates |
| `components` | string | no | Components the template is defined of |
| `componentType` | string | no | Determines the type of the component. Can be Header, Footer, Body, Buttons. |
| `text` | string | no | Template text |
| `format` | string | no | Which kind of header can be any of TEXT / IMAGE / DOCUMENT / VIDEO |
| `buttons[]` | array<object> | no | There can be up to 3 Quick reply buttons and Call to action buttons can be at most one of each button type for a maximum of 2 buttons. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "localizations": [
        [
          {}
        ]
      ],
      "templateCategory": "string",
      "templateName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `localizations[]` | array<object> |  |
| `localizations[].components[]` | array<object> |  |
| `localizations[].components[].text` | string |  |
| `localizations[].components[].type` | string |  |
| `localizations[].language` | string |  |
| `templateCategory` | string |  |
| `templateName` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /accounts/:whatsappAccountId/templates` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-whatsapp-template-for-review.md) for the provider-specific parameters and requirements.

