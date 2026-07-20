# Create Subscriber with Mailrelay

Creates a new subscriber in Mailrelay.

## Endpoint

- **Method:** `POST`
- **Path:** `subscribers`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Create Subscriber](https://apidocs.mailrelay.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | body | `string` | no | Subscriber country in ISO 3166-1 alpha-2 format. |
| `email` | body | `string` | yes | Subscriber email address. |
| `group_ids[]` | body | `array<number>` | no | Group IDs to assign to the subscriber. |
| `locale` | body | `string` | no | Subscriber locale. |
| `name` | body | `string` | no | Subscriber name. |
| `status` | body | `list` | yes | Initial subscriber status. Accepted values: `0`, `1`. |
| `time_zone` | body | `string` | no | Subscriber time zone. |
