# <img src="https://images.mindcloud.co/apps/icons/fraud-labs-pro_1775670083630.png" alt="FraudLabs Pro logo" width="28" height="28"> FraudLabs Pro: Universal API

Screen orders, users, SMS verification requests, and payment outcomes with FraudLabs Pro’s fraud-detection API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fraudLabsPro/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fraudlabspro.com/
- **Vendor API docs:** https://www.fraudlabspro.com/developer/api/screen-order

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Order Result](actions/get-order-result.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/get-order-result?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Verification Result](actions/get-verification-result.md) | GET | Retrieves an SMS verification result from FraudLabs Pro. |
| [Send SMS Verification](actions/send-sms-verification.md) | POST | Sends an SMS verification in FraudLabs Pro. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Feedback Order](actions/feedback-order.md) | PUT | Updates order feedback in FraudLabs Pro. |
| [Get Order Result](actions/get-order-result.md) | GET | Retrieves an order result from FraudLabs Pro. |
| [Screen Order](actions/screen-order.md) | POST | Screens an order for fraud in FraudLabs Pro. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Feedback Payment](actions/feedback-payment.md) | PUT | Updates payment feedback in FraudLabs Pro. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Feedback User](actions/feedback-user.md) | PUT | Updates user feedback in FraudLabs Pro. |
| [Get User Result](actions/get-user-result.md) | GET | Retrieves a user result from FraudLabs Pro. |
| [Screen User](actions/screen-user.md) | POST | Screens a user for fraud in FraudLabs Pro. |

