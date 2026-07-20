# Checkout Page: Get Checkout Page

Retrieves a checkout page from Checkout Page.

```
GET https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/get-checkout-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkout Page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/get-checkout-page?connectionId=$CONNECTION_ID&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/get-checkout-page?${params}`, {
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
| `pageId` | string | yes | Unique identifier. Must be in BSON ObjectId format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "afterPaymentAction": "string",
      "allowDynamicDescription": true,
      "allowDynamicDiscountedFromPrice": true,
      "allowDynamicPlanIterations": true,
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
      "enableFileAccessForInactiveSubscriptions": true,
      "fees": [
        {}
      ],
      "fields": [
        {}
      ],
      "funnelSteps": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "sellerId": "string",
      "slug": "string",
      "status": "string",
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
| `allowDynamicDescription` | boolean | Whether the description can be set dynamically via URL parameters. |
| `allowDynamicDiscountedFromPrice` | boolean | Whether the discounted from price can be set dynamically via URL parameters. |
| `allowDynamicPlanIterations` | boolean | Whether subscription plan iterations can be set dynamically via URL parameters. |
| `allowDynamicPrice` | boolean | Whether the price can be set dynamically via URL parameters. |
| `allowDynamicRedirectUrl` | boolean | Whether the redirect URL can be set dynamically via URL parameters. |
| `allowDynamicTitle` | boolean | Whether the title can be set dynamically via URL parameters. |
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
| `enableFileAccessForInactiveSubscriptions` | boolean | Whether customers with inactive subscriptions can still access digital files. |
| `fees` | array<object> | Extra fees applied at checkout. |
| `fields` | array<object> | Custom form fields on the page. |
| `funnelSteps` | array<object> | Ordered funnel steps for this page. The response uses the same public structure as the input schema, including `pageId` and `redirectPageId` field names. |
| `id` | string | Unique identifier. Must be in BSON ObjectId format. |
| `name` | string | Internal name of the page. |
| `sellerId` | string | Unique identifier. Must be in BSON ObjectId format. |
| `slug` | string | URL slug for the page. |
| `status` | string | Publication status of the page. |
| `type` | string | Type of page. |
| `updatedAt` | date | When the page was last updated. |
| `url` | string | Full URL to the hosted page. |

## Native endpoint

Through the native Checkout Page API, this operation is `GET /v1/checkout-pages/:pageId` (base URL `https://api.checkoutpage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-checkout-page.md) for the provider-specific parameters and requirements.

