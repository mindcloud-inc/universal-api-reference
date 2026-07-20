# Checkout Page: Get Form

Retrieves a form from Checkout Page.

```
GET https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/get-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkout Page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/get-form?connectionId=$CONNECTION_ID&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/get-form?${params}`, {
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
      "allowDynamicTitle": true,
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
      "fields": [
        {}
      ],
      "files": [
        {}
      ],
      "funnelSteps": [
        {}
      ],
      "googleIndex": true,
      "id": "string",
      "images": [
        {}
      ],
      "invoiceSettings": {},
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
| `allowDynamicDescription` | boolean | Whether the description can be set dynamically via URL parameters. |
| `allowDynamicTitle` | boolean | Whether the title can be set dynamically via URL parameters. |
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
| `fields` | array<object> | Custom form fields on the page. |
| `files` | array<object> | Downloadable files attached to this form page, available to customers after submission. |
| `funnelSteps` | array<object> | Ordered funnel steps for this page. The response uses the same public structure as the input schema, including `pageId` and `redirectPageId` field names. |
| `googleIndex` | boolean | Allow Google to index this page. |
| `id` | string | Unique identifier. Must be in BSON ObjectId format. |
| `images` | array<object> | Images displayed on the page. |
| `invoiceSettings` | object | Invoice configuration for manual payment flows. |
| `name` | string | Internal name of the page. |
| `sellerId` | string | Unique identifier. Must be in BSON ObjectId format. |
| `slug` | string | URL slug for the page. |
| `status` | string | Publication status of the page. |
| `title` | string | Display title shown on the page. |
| `type` | string | Type of page. |
| `updatedAt` | date | When the page was last updated. |
| `url` | string | Full URL to the hosted page. |

## Native endpoint

Through the native Checkout Page API, this operation is `GET /v1/forms/:pageId` (base URL `https://api.checkoutpage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form.md) for the provider-specific parameters and requirements.

