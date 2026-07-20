# Recurly Universal API Examples

These examples use the MindCloud API key and Recurly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sites



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recurly/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recurly/latest/actions/list-sites?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "features": [
        "string"
      ],
      "id": "string",
      "mode": "string",
      "object": "string",
      "publicApiKey": "string",
      "subdomain": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Sites action reference](actions/list-sites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/recurly/latest/actions/list-sites).

## Cancel Subscription



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recurly/latest/actions/cancel-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recurly/latest/actions/cancel-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptionId": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "account": {},
      "actionResult": {},
      "activatedAt": "2026-05-07T12:00:00.000Z",
      "activeInvoiceId": "string",
      "addOns": [
        {}
      ],
      "addOnsTotal": 1,
      "autoRenew": true,
      "billingInfoId": "string",
      "canceledAt": "2026-05-07T12:00:00.000Z",
      "collectionMethod": "string",
      "convertedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditApplicationPolicy": {},
      "currency": "string",
      "currentPeriodEndsAt": "2026-05-07T12:00:00.000Z",
      "currentPeriodStartedAt": "2026-05-07T12:00:00.000Z",
      "currentTermEndsAt": "2026-05-07T12:00:00.000Z",
      "currentTermStartedAt": "2026-05-07T12:00:00.000Z",
      "customerNotes": "string",
      "customFields": [
        {}
      ],
      "expirationReason": "string",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "gatewayCode": "string",
      "id": "string",
      "netTerms": 1,
      "netTermsType": "string",
      "nextAction": {},
      "object": "string",
      "pausedAt": "2026-05-07T12:00:00.000Z",
      "plan": {},
      "poNumber": "string",
      "priceSegmentId": "string",
      "quantity": 1,
      "rampIntervals": [
        {}
      ],
      "remainingBillingCycles": 1,
      "remainingPauseCycles": 1,
      "renewalBillingCycles": 1,
      "shipping": {},
      "startedWithGift": true,
      "state": "string",
      "subtotal": 1,
      "tax": 1,
      "taxInfo": {},
      "termsAndConditions": "string",
      "total": 1,
      "totalBillingCycles": 1,
      "trialEndsAt": "2026-05-07T12:00:00.000Z",
      "trialStartedAt": "2026-05-07T12:00:00.000Z",
      "unitAmount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Subscription action reference](actions/cancel-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/recurly/latest/actions/cancel-subscription).
