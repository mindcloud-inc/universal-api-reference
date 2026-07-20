# Update Subscriber with Mailrelay

Updates an existing subscriber in Mailrelay.

## Endpoint

- **Method:** `PATCH`
- **Path:** `subscribers/:id`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Update Subscriber](https://apidocs.mailrelay.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | body | `string` | no | Updated subscriber country in ISO 3166-1 alpha-2 format. |
| `group_ids[]` | body | `array<number>` | no | Updated group IDs for the subscriber. |
| `id` | path | `number` | yes | The Mailrelay subscriber ID. |
| `locale` | body | `string` | no | Updated subscriber locale. |
| `name` | body | `string` | no | Updated subscriber name. |
| `sms_phone` | body | `string` | no | Updated subscriber SMS phone number. |
| `time_zone` | body | `string` | no | Updated subscriber time zone. |
| `whatsapp_phone` | body | `string` | no | Updated subscriber WhatsApp phone number. |
