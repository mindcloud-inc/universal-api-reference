# <img src="https://images.mindcloud.co/apps/icons/ebulk-sms_1774985090883.png" alt="EbulkSMS logo" width="28" height="28"> EbulkSMS: Universal API

Send SMS and WhatsApp messages, check balance, and track delivery

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ebulkSMS/latest
- **Category:** Marketing
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ebulksms.com/
- **Vendor API docs:** https://www.ebulksms.com/pages/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Balance](actions/get-account-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebulkSMS/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Account Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Balance](actions/get-account-balance.md) | GET | Retrieves your EbulkSMS account balance. |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Get API Key](actions/get-api-key.md) | GET | Retrieves your EbulkSMS API key. |

### Sms Delivery Report

| Action | Method | Description |
| --- | --- | --- |
| [Get SMS Delivery Reports](actions/get-sms-delivery-reports.md) | GET | Retrieves SMS delivery reports from EbulkSMS. |

### Sms Message

| Action | Method | Description |
| --- | --- | --- |
| [Send SMS](actions/send-sms.md) | POST | Sends an SMS with EbulkSMS. |

### Whatsapp Delivery Report

| Action | Method | Description |
| --- | --- | --- |
| [Get WhatsApp Delivery Reports](actions/get-whatsapp-delivery-reports.md) | GET | Retrieves WhatsApp delivery reports from EbulkSMS. |

