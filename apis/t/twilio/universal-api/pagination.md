# Twilio Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Twilio expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-available-phone-number-countries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Twilio actions that support pagination

- [List Available Phone Number Countries](actions/list-available-phone-number-countries.md)
- [List Available Phone Numbers Local](actions/list-available-phone-numbers-local.md)
- [List Available Phone Numbers Mobile](actions/list-available-phone-numbers-mobile.md)
- [List Available Phone Numbers Toll-Free](actions/list-available-phone-numbers-toll-free.md)
- [List Incoming Phone Numbers](actions/list-incoming-phone-numbers.md)
- [List Messages](actions/list-messages.md)
- [List Messaging Pricing Countries](actions/list-messaging-pricing-countries.md)
- [List Messaging Service Alpha Senders](actions/list-messaging-service-alpha-senders.md)
- [List Messaging Service Channel Senders](actions/list-messaging-service-channel-senders.md)
- [List Messaging Service Destination Alpha Senders](actions/list-messaging-service-destination-alpha-senders.md)
- [List Messaging Service Phone Numbers](actions/list-messaging-service-phone-numbers.md)
- [List Messaging Service Short Codes](actions/list-messaging-service-short-codes.md)
- [List Messaging Services](actions/list-messaging-services.md)
