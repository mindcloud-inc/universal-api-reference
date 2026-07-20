# <img src="https://images.mindcloud.co/apps/icons/images-7_1774381575883.jpeg" alt="SparkPost logo" width="28" height="28"> SparkPost: Universal API

SparkPost is an email delivery platform for sending, managing, and analyzing transactional and marketing email.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sparkPost/latest
- **Category:** Communication / Email Communications
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sparkpost.com/
- **Vendor API docs:** https://developers.sparkpost.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Account](actions/retrieve-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/retrieve-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Account](actions/retrieve-account.md) | GET |  |
| [Update Account](actions/update-account.md) | PUT |  |

### Recipient List

| Action | Method | Description |
| --- | --- | --- |
| [Create Recipient List](actions/create-recipient-list.md) | POST |  |
| [List Recipient Lists](actions/list-recipient-lists.md) | GET |  |
| [Retrieve Recipient List](actions/retrieve-recipient-list.md) | GET |  |

### Sending Domain

| Action | Method | Description |
| --- | --- | --- |
| [Create Sending Domain](actions/create-sending-domain.md) | POST |  |
| [List Sending Domains](actions/list-sending-domains.md) | GET |  |
| [Retrieve Sending Domain](actions/retrieve-sending-domain.md) | GET |  |
| [Update Sending Domain](actions/update-sending-domain.md) | PUT |  |

### Sending Domain Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Sending Domain](actions/verify-sending-domain.md) | PUT |  |

### Subaccount

| Action | Method | Description |
| --- | --- | --- |
| [List Subaccounts](actions/list-subaccounts.md) | GET |  |

### Subaccounts Summary

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Subaccounts Summary](actions/retrieve-subaccounts-summary.md) | GET |  |

### Suppression

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Suppression](actions/retrieve-suppression.md) | GET |  |
| [Search Suppressions](actions/search-suppressions.md) | GET |  |

### Suppression Summary

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Suppression Summary](actions/retrieve-suppression-summary.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST |  |
| [List Templates](actions/list-templates.md) | GET |  |
| [Retrieve Template](actions/retrieve-template.md) | GET |  |
| [Update Draft Template](actions/update-draft-template.md) | PUT |  |

### Template Preview

| Action | Method | Description |
| --- | --- | --- |
| [Preview Template](actions/preview-template.md) | GET |  |

### Tracking Domain

| Action | Method | Description |
| --- | --- | --- |
| [Create Tracking Domain](actions/create-tracking-domain.md) | POST |  |
| [List Tracking Domains](actions/list-tracking-domains.md) | GET |  |
| [Retrieve Tracking Domain](actions/retrieve-tracking-domain.md) | GET |  |
| [Update Tracking Domain](actions/update-tracking-domain.md) | PUT |  |

### Tracking Domain Certificate Eligibility

| Action | Method | Description |
| --- | --- | --- |
| [Check Tracking Domain Certificate Eligibility](actions/check-tracking-domain-certificate-eligibility.md) | GET |  |

### Tracking Domain Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Tracking Domain](actions/verify-tracking-domain.md) | PUT |  |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Usage](actions/retrieve-usage.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

### Webhook Event Documentation

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Webhook Event Documentation](actions/retrieve-webhook-event-documentation.md) | GET |  |

### Webhook Event Samples

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Webhook Event Samples](actions/retrieve-webhook-event-samples.md) | GET |  |

