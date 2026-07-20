# <img src="https://images.mindcloud.co/apps/icons/date-time_1776429883898.png" alt="Date & Time logo" width="28" height="28"> Date & Time: Universal API

Read public IFTTT Date & Time service metadata, trigger definitions, and public applet catalog data from IFTTT’s official public GraphQL surface. This app documents the Date & Time service; it does not execute schedules itself.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dateTime/latest
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ifttt.com/date_and_time
- **Vendor API docs:** https://ifttt.com/date_and_time

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Date & Time Service Counts](actions/get-date-time-service-counts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dateTime/latest/actions/get-date-time-service-counts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Ifttt Applet

| Action | Method | Description |
| --- | --- | --- |
| [Get Public Applet By ID](actions/get-public-applet-by-id.md) | GET |  |
| [Get Public Applet Channels By ID](actions/get-public-applet-channels-by-id.md) | GET |  |
| [Get Public Applet Ingredients By ID](actions/get-public-applet-ingredients-by-id.md) | GET |  |
| [Get Public Applet Trigger By ID](actions/get-public-applet-trigger-by-id.md) | GET |  |
| [List Date & Time + Android SMS Applets](actions/list-date-time-android-sms-applets.md) | GET |  |
| [List Date & Time + Email Applets](actions/list-date-time-email-applets.md) | GET |  |
| [List Date & Time + Email Digest Applets](actions/list-date-time-email-digest-applets.md) | GET |  |
| [List Date & Time + Gmail Applets](actions/list-date-time-gmail-applets.md) | GET |  |
| [List Date & Time + iOS Reminders Applets](actions/list-date-time-ios-reminders-applets.md) | GET |  |
| [List Date & Time + LIFX Applets](actions/list-date-time-lifx-applets.md) | GET |  |
| [List Date & Time + Notifications Applets](actions/list-date-time-notifications-applets.md) | GET |  |
| [List Date & Time + Philips Hue Applets](actions/list-date-time-philips-hue-applets.md) | GET |  |
| [List Date & Time + Slack Applets](actions/list-date-time-slack-applets.md) | GET |  |
| [List Date & Time + X Applets](actions/list-date-time-x-applets.md) | GET |  |
| [List Public Applets For Date & Time](actions/list-public-applets-for-date-time.md) | GET |  |
| [List Public Applets For Trigger ID](actions/list-public-applets-for-trigger-id.md) | GET |  |

### Ifttt Service

| Action | Method | Description |
| --- | --- | --- |
| [Get Date & Time Service Counts](actions/get-date-time-service-counts.md) | GET |  |
| [Get Date & Time Service Flags](actions/get-date-time-service-flags.md) | GET |  |
| [Get Date & Time Service Overview](actions/get-date-time-service-overview.md) | GET |  |
| [List Date & Time Channel Snapshot](actions/list-date-time-channel-snapshot.md) | GET |  |

### Ifttt Trigger

| Action | Method | Description |
| --- | --- | --- |
| [Get Trigger Channel And Speed By ID](actions/get-trigger-channel-and-speed-by-id.md) | GET |  |
| [Get Trigger Channel And Speed By Module Name](actions/get-trigger-channel-and-speed-by-module-name.md) | GET |  |
| [Get Trigger Details By ID](actions/get-trigger-details-by-id.md) | GET |  |
| [Get Trigger Details By Module Name](actions/get-trigger-details-by-module-name.md) | GET |  |
| [Get Trigger Fields By ID](actions/get-trigger-fields-by-id.md) | GET |  |
| [Get Trigger Fields By Module Name](actions/get-trigger-fields-by-module-name.md) | GET |  |
| [Get Trigger Ingredients By ID](actions/get-trigger-ingredients-by-id.md) | GET |  |
| [Get Trigger Ingredients By Module Name](actions/get-trigger-ingredients-by-module-name.md) | GET |  |
| [List Date & Time Public Triggers](actions/list-date-time-public-triggers.md) | GET |  |
| [List Date & Time Trigger Modules](actions/list-date-time-trigger-modules.md) | GET |  |

