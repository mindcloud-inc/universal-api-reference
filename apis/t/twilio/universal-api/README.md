# <img src="https://images.mindcloud.co/apps/icons/icons8-twilio-96_1772647873034.png" alt="Twilio logo" width="28" height="28"> Twilio: Universal API

Send messages, make calls, verify users, and build communication workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/twilio/latest
- **Category:** Communication / Team Messaging
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.twilio.com
- **Vendor API docs:** https://www.twilio.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Messages](actions/list-messages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [List Messaging Service Channel Senders](actions/list-messaging-service-channel-senders.md) | GET | Retrieves messaging service channel senders from Twilio. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Available Phone Number Country](actions/get-available-phone-number-country.md) | GET | Retrieves available phone number details for a country in Twilio. |
| [List Available Phone Number Countries](actions/list-available-phone-number-countries.md) | GET | Retrieves available phone number countries from Twilio. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from Twilio. |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages from Twilio. |
| [Send Message](actions/send-message.md) | POST | Sends a new message with Twilio. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [List Available Phone Numbers Local](actions/list-available-phone-numbers-local.md) | GET | Finds available local phone numbers in Twilio. |
| [List Available Phone Numbers Mobile](actions/list-available-phone-numbers-mobile.md) | GET | Finds available mobile phone numbers in Twilio. |
| [List Available Phone Numbers Toll-Free](actions/list-available-phone-numbers-toll-free.md) | GET | Finds available toll-free phone numbers in Twilio. |
| [List Incoming Phone Numbers](actions/list-incoming-phone-numbers.md) | GET | Retrieves incoming phone numbers from Twilio. |
| [List Messaging Service Phone Numbers](actions/list-messaging-service-phone-numbers.md) | GET | Retrieves messaging service phone numbers from Twilio. |
| [List Messaging Service Short Codes](actions/list-messaging-service-short-codes.md) | GET | Retrieves messaging service short codes from Twilio. |

### Price

| Action | Method | Description |
| --- | --- | --- |
| [Get Messaging Pricing Country](actions/get-messaging-pricing-country.md) | GET | Retrieves messaging pricing for a country from Twilio. |
| [List Messaging Pricing Countries](actions/list-messaging-pricing-countries.md) | GET | Retrieves messaging country pricing from Twilio. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Create Messaging Service](actions/create-messaging-service.md) | POST | Creates a new messaging service in Twilio. |
| [Delete Messaging Service](actions/delete-messaging-service.md) | DELETE | Deletes an existing messaging service from Twilio. |
| [Get Messaging Service](actions/get-messaging-service.md) | GET | Retrieves a messaging service from Twilio. |
| [List Messaging Service Alpha Senders](actions/list-messaging-service-alpha-senders.md) | GET | Retrieves messaging service alpha senders from Twilio. |
| [List Messaging Service Destination Alpha Senders](actions/list-messaging-service-destination-alpha-senders.md) | GET | Retrieves messaging service destination alpha senders from Twilio. |
| [List Messaging Services](actions/list-messaging-services.md) | GET | Retrieves messaging services from Twilio. |
| [Update Messaging Service](actions/update-messaging-service.md) | PUT | Updates an existing messaging service in Twilio. |

