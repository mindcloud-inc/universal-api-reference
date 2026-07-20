# Checkout Page: Create Checkout Page

Creates a checkout page in Checkout Page.

```
POST https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/create-checkout-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkout Page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/create-checkout-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/create-checkout-page', {
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
| `slug` | string | no | Page URL slug. For events and forms the slug defaults to the slugified version of your `title`. For checkouts the slug defaults to the slugified version of your `productData.title`. |
| `status` | string | no | Initial publication status. Defaults to "published" if not provided. |
| `productData` | object | no | Product configuration for checkout pages. Use this object to define pricing mode, subscription/payment plan behavior, inventory, variants, and conditional variant visibility. Common setup patterns: - Standard one-time checkout: set `price.amount`, `price.currency`, and keep `price.pricingType` as `single`. - Variant-driven pricing: set `price.pricingType` to `multiple`, then define `variants` and per-option `additionalChargeAmount`. - Subscriptions (recurring): configure `price.recurring`. - Payment plans (fixed installments): configure `price.paymentPlan` with `planIterations`. Important rules: - You cannot set both `price.recurring` and `price.paymentPlan`. - `price.payWhatYouWant` cannot be used with subscriptions or payment plans. - `trialPeriodDays` and `startDate` are mutually exclusive within `recurring` and `paymentPlan`. - For conditional variant logic (`showHideLogic`) or `preselect`, set a `key` on variants/options to enable cross-references. Keys are not persisted. |
| `fields[]` | array<object> | no | Custom checkout fields to create. If one of your fields must be an `email` element and `required` must be true. Defaults to a name and email field if none are set. |
| `locale` | string | no | Locale code. |
| `customizeCheckoutConfirmation` | boolean | no | If set to true `confirmationCheckoutMessage` and `confirmationCheckoutTitle` will be displayed on the confirmation page. Defaults to `false`. |
| `allowDynamicTitle` | boolean | no | Allow page title to be overridden via URL query parameters. |
| `allowDynamicDescription` | boolean | no | Allow page description to be overridden via URL query parameters. |
| `closePopupOnClickOutside` | boolean | no | Whether a popup embed closes when clicking outside the container. Defaults to `false`. |
| `redirect` | object | no | If enabled, redirects the customer to the specified URL before the page loads. |
| `afterPaymentAction` | string | no | Behavior after checkout. `confirmation` shows the confirmation page. `checkout` redirects to `redirectPageId`. `redirect` sends the customer to `redirectUrl`. Defaults to `confirmation`. |

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

Through the native Checkout Page API, this operation is `POST /v1/checkout-pages/` (base URL `https://api.checkoutpage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-checkout-page.md) for the provider-specific parameters and requirements.

