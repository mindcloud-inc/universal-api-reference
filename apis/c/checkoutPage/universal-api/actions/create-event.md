# Checkout Page: Create Event

Creates a event in Checkout Page.

```
POST https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkout Page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Internal page name used in your dashboard and API responses. |
| `title` | string | no | Public title shown to customers on the page. |
| `slug` | string | no | Page URL slug. For events and forms the slug defaults to the slugified version of your `title`. For checkouts the slug defaults to the slugified version of your `productData.title`. |
| `description` | string | no | Page description shown to customers. Accepts HTML or plain text. |
| `status` | string | no | Initial publication status. Defaults to "published" if not provided. |
| `fields[]` | array<object> | no | Custom checkout fields to create. If one of your fields must be an `email` element and `required` must be true. Defaults to a name and email field if none are set. |
| `locale` | string | no | Locale code. |
| `customizeCheckoutConfirmation` | boolean | no | If set to true `confirmationCheckoutMessage` and `confirmationCheckoutTitle` will be displayed on the confirmation page. Defaults to `false`. |
| `allowDynamicTitle` | boolean | no | Allow page title to be overridden via URL query parameters. |
| `allowDynamicDescription` | boolean | no | Allow page description to be overridden via URL query parameters. |
| `closePopupOnClickOutside` | boolean | no | Whether a popup embed closes when clicking outside the container. Defaults to `false`. |
| `redirect` | object | no | If enabled, redirects the customer to the specified URL before the page loads. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "afterPaymentAction": "string",
      "allowDynamicDescription": true,
      "allowDynamicDiscountedFromPrice": true,
      "allowDynamicPrice": true,
      "allowDynamicRedirectUrl": true,
      "allowDynamicTitle": true,
      "checkoutAbandonment": {},
      "closePopupOnClickOutside": true,
      "confirmationCheckoutMessage": "string",
      "confirmationCheckoutTitle": "string",
      "confirmationEmailMessage": "ava@example.com",
      "confirmationEmailShowLogo": true,
      "confirmationEmailShowStoreName": true,
      "confirmationEmailSubject": "ava@example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customizeCheckoutConfirmation": true,
      "customizeEmailConfirmation": true,
      "description": "string",
      "descriptionHtml": "string",
      "eventDetails": {},
      "fees": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "sellerId": "string",
      "slug": "string",
      "status": "string",
      "title": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `afterPaymentAction` | string | Behavior after checkout. |
| `allowDynamicDescription` | boolean | Whether the description can be overridden via URL query parameters. |
| `allowDynamicDiscountedFromPrice` | boolean | Whether the compare-at price can be overridden via URL query parameters. |
| `allowDynamicPrice` | boolean | Whether the price can be overridden via URL query parameters. |
| `allowDynamicRedirectUrl` | boolean | Whether the redirect URL can be overridden via URL query parameters. |
| `allowDynamicTitle` | boolean | Whether the title can be overridden via URL query parameters. |
| `checkoutAbandonment` | object | Checkout abandonment email reminder settings. |
| `closePopupOnClickOutside` | boolean | Whether a popup embed closes when clicking outside the container. |
| `confirmationCheckoutMessage` | string | Confirmation page message. |
| `confirmationCheckoutTitle` | string | Confirmation page title. |
| `confirmationEmailMessage` | string | Custom confirmation email message. |
| `confirmationEmailShowLogo` | boolean | Show store logo in confirmation email. |
| `confirmationEmailShowStoreName` | boolean | Show store name in confirmation email. |
| `confirmationEmailSubject` | string | Custom confirmation email subject. |
| `createdAt` | date | When the page was created. |
| `customizeCheckoutConfirmation` | boolean | If set to true `confirmationCheckoutMessage` and `confirmationCheckoutTitle` will be displayed on the confirmation page. Defaults to `false`. |
| `customizeEmailConfirmation` | boolean | Use a custom email confirmation template. |
| `description` | string | Page description stored as Lexical rich text JSON. |
| `descriptionHtml` | string | HTML description of the page. |
| `eventDetails` | object | Event-specific details. |
| `fees` | array<object> | Extra fees applied at checkout. |
| `id` | string | Unique identifier. Must be in BSON ObjectId format. |
| `name` | string | Internal name of the page. |
| `sellerId` | string | Unique identifier. Must be in BSON ObjectId format. |
| `slug` | string | URL slug for the page. |
| `status` | string | Publication status of the page. |
| `title` | string | Display title shown on the page. |
| `type` | string | Type of page. |
| `updatedAt` | date | When the page was last updated. |
| `url` | string | Full URL to the hosted page. |

## Native endpoint

Through the native Checkout Page API, this operation is `POST /v1/events/` (base URL `https://api.checkoutpage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

