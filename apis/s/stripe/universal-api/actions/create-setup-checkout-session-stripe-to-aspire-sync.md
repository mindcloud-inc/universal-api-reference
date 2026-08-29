# Stripe: Create Setup Checkout Session – Stripe to Aspire Sync



```
POST https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-setup-checkout-session-stripe-to-aspire-sync
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-setup-checkout-session-stripe-to-aspire-sync" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "successUrl": "https://example.com",
  "cancelUrl": "https://example.com",
  "paymentMethodTypes[]": [
    "string"
  ],
  "clientReferenceId": "string",
  "contractVersion": "string",
  "mindcloudRequestId": "string",
  "paymentKind": "string",
  "aspireOpportunityNumber": "string",
  "aspireOpportunityRevision": "string",
  "aspireBillingCompany": "string",
  "aspireBillingContact": "string",
  "aspireProperty": "string",
  "aspireBranchName": "Ava Chen",
  "aspireInvoiceNumber": "string",
  "depositPercent": "string",
  "depositBasisCents": "string",
  "serviceAmountCents": "string",
  "serviceTaxCents": "string",
  "cardFeeCents": "string",
  "cardFeeTaxCents": "string",
  "currency": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-setup-checkout-session-stripe-to-aspire-sync', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "successUrl": "https://example.com",
    "cancelUrl": "https://example.com",
    "paymentMethodTypes[]": ["string"],
    "clientReferenceId": "string",
    "contractVersion": "string",
    "mindcloudRequestId": "string",
    "paymentKind": "string",
    "aspireOpportunityNumber": "string",
    "aspireOpportunityRevision": "string",
    "aspireBillingCompany": "string",
    "aspireBillingContact": "string",
    "aspireProperty": "string",
    "aspireBranchName": "Ava Chen",
    "aspireInvoiceNumber": "string",
    "depositPercent": "string",
    "depositBasisCents": "string",
    "serviceAmountCents": "string",
    "serviceTaxCents": "string",
    "cardFeeCents": "string",
    "cardFeeTaxCents": "string",
    "currency": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer` | string | no | Stripe Customer ID, supplied dynamically. |
| `customerEmail` | string | no | Customer email when no Stripe Customer ID is supplied. |
| `successUrl` | string | yes | Hosted Checkout success redirect URL. |
| `cancelUrl` | string | yes | Hosted Checkout cancellation redirect URL. |
| `paymentMethodTypes[]` | array<string> | yes | Allowed Stripe payment method types. Each value must be card or us_bank_account. Accepts multiple values as an array. |
| `clientReferenceId` | string | yes | Unique MindCloud request ID used to reconcile the Checkout Session. |
| `contractVersion` | string | yes | Exact Stripe to Aspire metadata contract version. |
| `mindcloudRequestId` | string | yes | Unique request identifier matching the payment reference contract. |
| `paymentKind` | string | yes | Payment kind: deposit or invoice. |
| `aspireOpportunityNumber` | string | yes | Aspire Opportunity number audit link. |
| `aspireOpportunityRevision` | string | yes | Aspire Opportunity revision. |
| `aspireBillingCompany` | string | yes | Aspire billing company; use the exact non-empty sentinel "none" only when the billing contact is populated. |
| `aspireBillingContact` | string | yes | Aspire billing contact; use the exact non-empty sentinel "none" only when the billing company is populated. |
| `aspireProperty` | string | yes | Aspire property audit context. |
| `aspireBranchName` | string | yes | Aspire branch name. |
| `aspireInvoiceNumber` | string | yes | Use the exact non-empty sentinel "none" for deposits; use a positive integer string for invoice payments. |
| `depositPercent` | string | yes | Deposit percentage string for deposits; use the exact non-empty sentinel "none" for invoice payments. |
| `depositBasisCents` | string | yes | Positive canonical integer-cent basis for deposits; use the exact non-empty sentinel "none" for invoice payments. |
| `serviceAmountCents` | string | yes | Canonical non-negative integer service amount in cents. |
| `serviceTaxCents` | string | yes | Canonical non-negative integer service sales tax in cents. |
| `cardFeeCents` | string | yes | Canonical non-negative integer customer card fee in cents. |
| `cardFeeTaxCents` | string | yes | Canonical non-negative integer sales tax on the card fee in cents. |
| `currency` | string | yes | Exact lowercase metadata currency code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountTotal": 1,
      "created": 1,
      "currency": "string",
      "customer": "string",
      "id": "string",
      "mode": "string",
      "object": "string",
      "paymentStatus": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountTotal` | number | Total amount in integer cents |
| `created` | number | Creation timestamp in seconds |
| `currency` | string | Session currency |
| `customer` | string | Stripe Customer ID |
| `id` | string | Checkout session ID |
| `mode` | string | Checkout mode |
| `object` | string | Stripe object type |
| `paymentStatus` | string | Payment status |
| `status` | string | Session status |
| `url` | string | Hosted checkout URL |

## Native endpoint

Through the native Stripe API, this operation is `POST checkout/sessions` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-setup-checkout-session-stripe-to-aspire-sync.md) for the provider-specific parameters and requirements.

