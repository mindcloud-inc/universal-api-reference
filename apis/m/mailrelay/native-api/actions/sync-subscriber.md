# Sync Subscriber with Mailrelay

Finds a subscriber in Mailrelay, or creates one if no match is found.

## Endpoint

- **Method:** `POST`
- **Path:** `subscribers/sync`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Sync Subscriber](https://apidocs.mailrelay.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Subscriber email for sync. |
| `group_ids[]` | body | `array<number>` | no | Group IDs to assign during sync. |
| `replace_groups` | body | `boolean` | no | Whether to replace existing groups when syncing an existing subscriber. |
| `status` | body | `list` | yes | Subscriber status for sync. Accepted values: `0`, `1`. |
