# <img src="https://images.mindcloud.co/apps/icons/id-ooc-iebj-t-logos_1777311700817.png" alt="Raklet logo" width="28" height="28"> Raklet: Universal API

Manage members, memberships, and community workflows in Raklet

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/raklet/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.raklet.com/
- **Vendor API docs:** https://help.raklet.com/en/collections/13838830-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get organisation settings](actions/get-organisation-settings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raklet/latest/actions/get-organisation-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | POST |  |

### Board

| Action | Method | Description |
| --- | --- | --- |
| [List Boards](actions/list-boards.md) | GET |  |

### Contact Address

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact Address](actions/add-contact-address.md) | POST |  |
| [Delete Contact Address](actions/delete-contact-address.md) | DELETE |  |
| [Set Primary Contact Address](actions/set-primary-contact-address.md) | PUT |  |
| [Update Contact Address](actions/update-contact-address.md) | PUT |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [Get Contact Details](actions/get-contact-details.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Debt

| Action | Method | Description |
| --- | --- | --- |
| [Create Debt](actions/create-debt.md) | POST |  |
| [Get Debt](actions/get-debt.md) | GET |  |
| [List Debts](actions/list-debts.md) | GET |  |

### Donation

| Action | Method | Description |
| --- | --- | --- |
| [Create Donation](actions/create-donation.md) | POST |  |
| [Get Donation](actions/get-donation.md) | GET |  |
| [List Donations](actions/list-donations.md) | GET |  |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact Email](actions/add-contact-email.md) | POST |  |
| [Delete Contact Email](actions/delete-contact-email.md) | DELETE |  |
| [Set Primary Contact Email](actions/set-primary-contact-email.md) | PUT |  |
| [Update Contact Email](actions/update-contact-email.md) | PUT |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET |  |
| [List Events](actions/list-events.md) | GET |  |

### Organisation Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get organisation settings](actions/get-organisation-settings.md) | GET |  |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment](actions/create-payment.md) | POST |  |
| [Get Payment](actions/get-payment.md) | GET |  |
| [List Payments](actions/list-payments.md) | GET |  |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact Phone](actions/add-contact-phone.md) | POST |  |
| [Delete Contact Phone](actions/delete-contact-phone.md) | DELETE |  |
| [Set Primary Contact Phone](actions/set-primary-contact-phone.md) | PUT |  |
| [Update Contact Phone](actions/update-contact-phone.md) | PUT |  |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | POST |  |
| [List Posts](actions/list-posts.md) | GET |  |

### Subscription Plans

| Action | Method | Description |
| --- | --- | --- |
| [Get Plan](actions/get-plan.md) | GET |  |
| [List Plans](actions/list-plans.md) | GET |  |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST |  |
| [Delete Subscription](actions/delete-subscription.md) | DELETE |  |
| [Get Subscription](actions/get-subscription.md) | GET |  |
| [List Subscriptions](actions/list-subscriptions.md) | GET |  |
| [Update Subscription](actions/update-subscription.md) | PUT |  |

