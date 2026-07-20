# <img src="https://images.mindcloud.co/apps/icons/outseta_1773840096750.png" alt="Outseta logo" width="28" height="28"> Outseta: Universal API

Manage memberships, CRM, billing, and member email with Outseta

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/outseta/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.outseta.com
- **Vendor API docs:** https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Billing Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Add New Invoice](actions/add-new-invoice.md) | POST | Creates a new invoice in Outseta. |

### Billing Invoice Preview

| Action | Method | Description |
| --- | --- | --- |
| [Add First Time Subscription Preview](actions/add-first-time-subscription-preview.md) | POST | Retrieves a first-time subscription charge preview from Outseta. |
| [Change Subscription Preview](actions/change-subscription-preview.md) | PUT | Retrieves a subscription change preview from Outseta. |

### Billing Plan

| Action | Method | Description |
| --- | --- | --- |
| [List Plans](actions/list-plans.md) | GET | Retrieves a list of plans from Outseta. |

### Billing Plan Family

| Action | Method | Description |
| --- | --- | --- |
| [List Plan Families](actions/list-plan-families.md) | GET | Retrieves a list of plan families from Outseta. |

### Billing Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Add Add-On to Subscription](actions/add-add-on-to-subscription.md) | POST | Adds an add-on to a subscription in Outseta. |
| [Add Discount to Subscription](actions/add-discount-to-subscription.md) | POST | Adds a discount to a subscription in Outseta. |
| [Add First Time Subscription](actions/add-first-time-subscription.md) | PUT | Adds a first-time subscription in Outseta. |
| [Change Subscription](actions/change-subscription.md) | PUT | Changes an existing subscription in Outseta. |
| [Extend Trial Subscription](actions/extend-trial-subscription.md) | PUT | Extends a trial subscription in Outseta. |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves a subscription from Outseta. |

### Billing Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Add Invoice Payment](actions/add-invoice-payment.md) | POST | Creates an invoice payment in Outseta. |
| [List Transactions by Account](actions/list-transactions-by-account.md) | GET | Retrieves account transactions from Outseta. |

### Crm Account

| Action | Method | Description |
| --- | --- | --- |
| [Add Account with Existing Person](actions/add-account-with-existing-person.md) | POST | Creates an account with an existing person in Outseta. |
| [Add Account with New Person](actions/add-account-with-new-person.md) | POST | Creates an account with a new person in Outseta. |
| [Add Account with Subscription](actions/add-account-with-subscription.md) | POST | Creates an account with a subscription in Outseta. |
| [Add Existing Person to Existing Account](actions/add-existing-person-to-existing-account.md) | POST | Adds an existing person to an existing account in Outseta. |
| [Add New Person to Existing Account](actions/add-new-person-to-existing-account.md) | POST | Adds a new person to an existing account in Outseta. |
| [Cancel Account](actions/cancel-account.md) | PUT | Cancels an existing account in Outseta. |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from Outseta. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves a list of accounts from Outseta. |
| [Register Account](actions/register-account.md) | POST | Registers an account in Outseta. |
| [Remove Cancellation](actions/remove-cancellation.md) | PUT | Removes an account cancellation in Outseta. |
| [Update Account](actions/update-account.md) | PUT | Updates an existing account in Outseta. |

### Crm Account Membership

| Action | Method | Description |
| --- | --- | --- |
| [Remove Person from Account](actions/remove-person-from-account.md) | DELETE | Removes a person from an account in Outseta. |
| [Update Person Account Membership](actions/update-person-account-membership.md) | PUT | Updates an existing account membership in Outseta. |

### Crm Activity

| Action | Method | Description |
| --- | --- | --- |
| [Add Custom Activity](actions/add-custom-activity.md) | POST | Creates a custom activity in Outseta. |
| [List Activities](actions/list-activities.md) | GET | Retrieves a list of activities from Outseta. |

### Crm Deal

| Action | Method | Description |
| --- | --- | --- |
| [Add Deal](actions/add-deal.md) | POST | Creates a new deal in Outseta. |
| [Delete Deal](actions/delete-deal.md) | DELETE | Deletes an existing deal from Outseta. |
| [Get Deal](actions/get-deal.md) | GET | Retrieves a deal from Outseta. |
| [List Deals](actions/list-deals.md) | GET | Retrieves a list of deals from Outseta. |
| [Update Deal](actions/update-deal.md) | PUT | Updates an existing deal in Outseta. |

### Crm Person

| Action | Method | Description |
| --- | --- | --- |
| [Add Person](actions/add-person.md) | POST | Creates a new person in Outseta. |
| [Delete Person](actions/delete-person.md) | DELETE | Deletes an existing person from Outseta. |
| [Get Person](actions/get-person.md) | GET | Retrieves a person from Outseta. |
| [Initiate Password Reset](actions/initiate-password-reset.md) | POST | Initiates a password reset for a person in Outseta. |
| [List People](actions/list-people.md) | GET | Retrieves a list of people from Outseta. |
| [Set Temporary Password](actions/set-temporary-password.md) | PUT | Sets a temporary password for a person in Outseta. |
| [Update Person](actions/update-person.md) | PUT | Updates an existing person in Outseta. |

