# Twilio: Native API Reference

A consolidated summary of Twilio's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://www.twilio.com/docs
- **OpenAPI specification:** https://raw.githubusercontent.com/twilio/twilio-oai/main/spec/json/twilio_api_v2010.json
- **API base URL:** `https://api.twilio.com/2010-04-01`

## Authentication

### API Key SID / API Key Secret

Enter TWILIO_API_KEY_SID in Username and TWILIO_API_KEY_SECRET in Password. Account SID and messaging metadata are captured in additional fields.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Scopes:** `scopes` · optional
- **Twilio Phone Number:** `twilioPhoneNumber` · optional
- **Twilio Messaging Service SID:** `twilioMessagingServiceSid` · optional

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.twilio.com/docs/iam/api-keys)

## API conventions

Responses from this API use JSON. The next-page cursor is read from `next_page_uri`. The current page number is read from `page`.

## Pagination

Use `PageSize` in the query string to set the page size (default 50; accepted range 1–1000). Use `Page` in the query string to choose the page; numbering starts at 0.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Messaging Service](actions/create-messaging-service.md) | `POST https://messaging.twilio.com/v1/Services` | [docs](https://www.twilio.com/docs/messaging/api/service-resource#create-a-service) |
| [Delete Messaging Service](actions/delete-messaging-service.md) | `DELETE https://messaging.twilio.com/v1/Services/:Sid` | [docs](https://www.twilio.com/docs/messaging/api/service-resource#delete-a-service) |
| [Get Available Phone Number Country](actions/get-available-phone-number-country.md) | `GET /Accounts/:AccountSid/AvailablePhoneNumbers/:CountryCode.json` | [docs](https://www.twilio.com/docs/phone-numbers/api/availablephonenumber-resource#fetch-a-specific-country) |
| [Get Message](actions/get-message.md) | `GET /Accounts/:AccountSid/Messages/:MessageSid.json` | [docs](https://www.twilio.com/docs/messaging/api/message-resource#fetch-a-message-resource) |
| [Get Messaging Pricing Country](actions/get-messaging-pricing-country.md) | `GET https://pricing.twilio.com/v1/Messaging/Countries/:IsoCountry` | [docs](https://www.twilio.com/docs/messaging/api/pricing#fetch-a-countries-resource) |
| [Get Messaging Service](actions/get-messaging-service.md) | `GET https://messaging.twilio.com/v1/Services/:Sid` | [docs](https://www.twilio.com/docs/messaging/api/service-resource#retrieve-a-service) |
| [List Available Phone Number Countries](actions/list-available-phone-number-countries.md) | `GET /Accounts/:AccountSid/AvailablePhoneNumbers.json` | [docs](https://www.twilio.com/docs/phone-numbers/api/availablephonenumber-resource#read-a-list-of-countries) |
| [List Available Phone Numbers Local](actions/list-available-phone-numbers-local.md) | `GET /Accounts/:AccountSid/AvailablePhoneNumbers/:CountryCode/Local.json` | [docs](https://www.twilio.com/docs/phone-numbers/api/availablephonenumberlocal-resource#read-multiple-availablephonenumberlocal-resources) |
| [List Available Phone Numbers Mobile](actions/list-available-phone-numbers-mobile.md) | `GET /Accounts/:AccountSid/AvailablePhoneNumbers/:CountryCode/Mobile.json` | [docs](https://www.twilio.com/docs/phone-numbers/api/availablephonenumber-mobile-resource#read-multiple-availablephonenumbermobile-resources) |
| [List Available Phone Numbers Toll-Free](actions/list-available-phone-numbers-toll-free.md) | `GET /Accounts/:AccountSid/AvailablePhoneNumbers/:CountryCode/TollFree.json` | [docs](https://www.twilio.com/docs/phone-numbers/api/availablephonenumber-tollfree-resource#read-multiple-availablephonenumbertollfree-resources) |
| [List Incoming Phone Numbers](actions/list-incoming-phone-numbers.md) | `GET /Accounts/:AccountSid/IncomingPhoneNumbers.json` | [docs](https://www.twilio.com/docs/phone-numbers/api/incomingphonenumber-resource#read-multiple-incomingphonenumber-resources) |
| [List Messages](actions/list-messages.md) | `GET /Accounts/:AccountSid/Messages.json` | [docs](https://www.twilio.com/docs/messaging/api/message-resource#read-multiple-message-resources) |
| [List Messaging Pricing Countries](actions/list-messaging-pricing-countries.md) | `GET https://pricing.twilio.com/v1/Messaging/Countries` | [docs](https://www.twilio.com/docs/messaging/api/pricing#read-multiple-countries-resources) |
| [List Messaging Service Alpha Senders](actions/list-messaging-service-alpha-senders.md) | `GET https://messaging.twilio.com/v1/Services/:ServiceSid/AlphaSenders` | [docs](https://www.twilio.com/docs/messaging/api/alphasender-resource#retrieve-a-list-of-alphasenders) |
| [List Messaging Service Channel Senders](actions/list-messaging-service-channel-senders.md) | `GET https://messaging.twilio.com/v1/Services/:ServiceSid/ChannelSenders` | [docs](https://www.twilio.com/docs/messaging/api/messaging-service-channelsender-resource#retrieve-a-list-of-channelsenders) |
| [List Messaging Service Destination Alpha Senders](actions/list-messaging-service-destination-alpha-senders.md) | `GET https://messaging.twilio.com/v1/Services/:ServiceSid/DestinationAlphaSenders` | [docs](https://www.twilio.com/docs/messaging/api/destination-alphasender-resource#retrieve-a-list-of-destinationalphasenders) |
| [List Messaging Service Phone Numbers](actions/list-messaging-service-phone-numbers.md) | `GET https://messaging.twilio.com/v1/Services/:ServiceSid/PhoneNumbers` | [docs](https://www.twilio.com/docs/messaging/api/phonenumber-resource#retrieve-a-list-of-phonenumbers) |
| [List Messaging Service Short Codes](actions/list-messaging-service-short-codes.md) | `GET https://messaging.twilio.com/v1/Services/:ServiceSid/ShortCodes` | [docs](https://www.twilio.com/docs/messaging/api/services-shortcode-resource#retrieve-a-list-of-shortcodes) |
| [List Messaging Services](actions/list-messaging-services.md) | `GET https://messaging.twilio.com/v1/Services` | [docs](https://www.twilio.com/docs/messaging/api/service-resource#retrieve-a-list-of-services) |
| [Send Message](actions/send-message.md) | `POST /Accounts/:AccountSid/Messages.json` | [docs](https://www.twilio.com/docs/messaging/api/message-resource#create-a-message-resource) |
| [Update Messaging Service](actions/update-messaging-service.md) | `POST https://messaging.twilio.com/v1/Services/:Sid` | [docs](https://www.twilio.com/docs/messaging/api/service-resource#update-a-service) |
