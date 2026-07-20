# <img src="https://images.mindcloud.co/apps/icons/go-daddy-crm_1774541140907.png" alt="GoDaddy CRM logo" width="28" height="28"> GoDaddy CRM: Universal API

Manage GoDaddy shoppers, domains, and account data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/goDaddyCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 39
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.godaddy.com
- **Vendor API docs:** https://developer.godaddy.com/doc

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Orders](actions/list-orders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (39)

### Certificate

| Action | Method | Description |
| --- | --- | --- |
| [Download Certificate](actions/download-certificate.md) | GET | Downloads a customer certificate from GoDaddy. |
| [List Customer Certificates](actions/list-customer-certificates.md) | GET | Retrieves certificates for a GoDaddy customer. |
| [Search Certificates](actions/search-certificates.md) | GET | Retrieves certificates from your GoDaddy account. |

### Dns Record

| Action | Method | Description |
| --- | --- | --- |
| [Add DNS Records](actions/add-dns-records.md) | PUT | Adds DNS records to a GoDaddy domain. |
| [Delete DNS Records By Type And Name](actions/delete-dns-records-by-type-and-name.md) | DELETE | Deletes DNS records from a GoDaddy domain. |
| [Get DNS Records](actions/get-dns-records.md) | GET | Retrieves DNS records for a GoDaddy domain. |
| [Replace All DNS Records](actions/replace-all-dns-records.md) | PUT | Replaces all DNS records for a GoDaddy domain. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Check Domain Availability](actions/check-domain-availability.md) | GET | Checks domain availability with the GoDaddy API. |
| [Get Domain Registration Schema](actions/get-domain-registration-schema.md) | GET | Retrieves a domain registration schema from GoDaddy. |
| [Get Domain Transfer Status](actions/get-domain-transfer-status.md) | GET | Retrieves domain transfer status from GoDaddy. |
| [List Domains](actions/list-domains.md) | GET | Retrieves domains from your GoDaddy account. |
| [List Supported TLDs](actions/list-supported-tlds.md) | GET | Retrieves supported TLDs from the GoDaddy API. |
| [Register Domain](actions/register-domain.md) | POST | Registers a domain for a GoDaddy customer. |
| [Renew Domain](actions/renew-domain.md) | POST | Renews a domain in your GoDaddy account. |
| [Retrieve Domain Details](actions/retrieve-domain-details.md) | GET | Retrieves domain details from your GoDaddy account. |
| [Retrieve Domain Purchase Agreements](actions/retrieve-domain-purchase-agreements.md) | GET | Retrieves domain purchase agreements from GoDaddy. |
| [Retry Domain Transfer In](actions/retry-domain-transfer-in.md) | POST | Retries a domain transfer into GoDaddy. |
| [Start Domain Transfer In](actions/start-domain-transfer-in.md) | POST | Starts a domain transfer into GoDaddy. |
| [Suggest Domains](actions/suggest-domains.md) | GET | Suggests domains with the GoDaddy API. |
| [Update Domain Details](actions/update-domain-details.md) | PUT | Updates a domain's details in GoDaddy. |
| [Validate Domain Registration](actions/validate-domain-registration.md) | POST | Validates a domain registration in GoDaddy. |
| [Validate Domain Transfer](actions/validate-domain-transfer.md) | POST | Validates a domain transfer in GoDaddy. |

### Domain Action

| Action | Method | Description |
| --- | --- | --- |
| [List Domain Actions](actions/list-domain-actions.md) | GET | Retrieves actions for a GoDaddy domain. |

### Domain Contact

| Action | Method | Description |
| --- | --- | --- |
| [Update Domain Contacts](actions/update-domain-contacts.md) | PUT | Updates contacts for a GoDaddy domain. |

### Domain Privacy

| Action | Method | Description |
| --- | --- | --- |
| [Purchase Domain Privacy](actions/purchase-domain-privacy.md) | POST | Purchases domain privacy for a GoDaddy domain. |

### Nameserver

| Action | Method | Description |
| --- | --- | --- |
| [Replace Nameservers](actions/replace-nameservers.md) | PUT | Replaces nameservers for a GoDaddy domain. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [List Orders](actions/list-orders.md) | GET | Retrieves customer orders from your GoDaddy account. |
| [Retrieve Order Details](actions/retrieve-order-details.md) | GET | Retrieves order details from your GoDaddy account. |

### Privacy Forwarding

| Action | Method | Description |
| --- | --- | --- |
| [Get Privacy Forwarding Settings](actions/get-privacy-forwarding-settings.md) | GET | Retrieves privacy forwarding settings for a GoDaddy domain. |
| [Update Privacy Forwarding Settings](actions/update-privacy-forwarding-settings.md) | PUT | Updates privacy forwarding settings for a GoDaddy domain. |

### Shopper

| Action | Method | Description |
| --- | --- | --- |
| [Create Shopper Subaccount](actions/create-shopper-subaccount.md) | POST | Creates a shopper subaccount in GoDaddy. |
| [Get Shopper Details](actions/get-shopper-details.md) | GET | Retrieves shopper details from your GoDaddy account. |
| [Update Shopper Details](actions/update-shopper-details.md) | PUT | Updates shopper details in your GoDaddy account. |

### Shopper Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Shopper Status](actions/get-shopper-status.md) | GET | Retrieves shopper status from your GoDaddy account. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | DELETE | Cancels an existing subscription in GoDaddy. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from your GoDaddy account. |
| [Retrieve Subscription Details](actions/retrieve-subscription-details.md) | GET | Retrieves subscription details from your GoDaddy account. |
| [Update Subscription](actions/update-subscription.md) | PUT | Updates an existing subscription in GoDaddy. |

### Subscription Product Group

| Action | Method | Description |
| --- | --- | --- |
| [List Subscription Product Groups](actions/list-subscription-product-groups.md) | GET | Retrieves subscription product groups from GoDaddy. |

