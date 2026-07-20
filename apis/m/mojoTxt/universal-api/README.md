# <img src="https://images.mindcloud.co/apps/icons/images-8_1774455381900.jpeg" alt="MojoTxt logo" width="28" height="28"> MojoTxt: Universal API

Send texts, manage subscribers, and track donations and lists

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mojoTxt/latest
- **Category:** Communication / Team Messaging
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mojotxt.com
- **Vendor API docs:** https://app.mojotxt.com/api/docs/v1/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Export Donations](actions/export-donations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/export-donations?connectionId=$CONNECTION_ID&limit=25&offset=0&donationIdOrKeyword=string&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Donation Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Donations](actions/export-donations.md) | GET | Retrieves a donation export from MojoTxt. |

### Donation Keyword

| Action | Method | Description |
| --- | --- | --- |
| [Create Donation Keyword](actions/create-donation-keyword.md) | POST | Creates a donation keyword in MojoTxt. |
| [Delete Donation](actions/delete-donation.md) | DELETE | Deletes a donation from MojoTxt. |
| [Get Donation](actions/get-donation.md) | GET | Retrieves a donation from MojoTxt. |
| [List Donations](actions/list-donations.md) | GET | Retrieves donations for a MojoTxt phone number. |
| [Update Donation Keyword](actions/update-donation-keyword.md) | PUT | Updates a donation keyword in MojoTxt. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | POST | Creates a message in MojoTxt. |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes a message from MojoTxt. |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from MojoTxt. |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages for a MojoTxt phone number. |
| [Update Message](actions/update-message.md) | PUT | Updates a message in MojoTxt. |

### Message Log

| Action | Method | Description |
| --- | --- | --- |
| [List Message Log](actions/list-message-log.md) | GET | Retrieves a message log from MojoTxt. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [List Phone Numbers](actions/list-phone-numbers.md) | GET | Retrieves phone numbers from MojoTxt. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [List Phone Number Subscribers](actions/list-phone-number-subscribers.md) | GET | Retrieves subscribers for a MojoTxt phone number. |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves subscribers from MojoTxt. |

### Subscription List

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription List](actions/create-subscription-list.md) | POST | Creates a subscription list in MojoTxt. |
| [Delete Subscription List](actions/delete-subscription-list.md) | DELETE | Deletes a subscription list from MojoTxt. |
| [Get Subscription List](actions/get-subscription-list.md) | GET | Retrieves a subscription list from MojoTxt. |
| [List Subscription Lists](actions/list-subscription-lists.md) | GET | Retrieves subscription lists from MojoTxt. |
| [Update Subscription List](actions/update-subscription-list.md) | PUT | Updates a subscription list in MojoTxt. |

