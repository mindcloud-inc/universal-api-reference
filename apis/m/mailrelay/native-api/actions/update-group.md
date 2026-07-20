# Update Group with Mailrelay

Updates an existing subscriber group in Mailrelay.

## Endpoint

- **Method:** `PATCH`
- **Path:** `groups/:id`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Update Group](https://apidocs.mailrelay.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Updated group description. |
| `id` | path | `number` | yes | The Mailrelay group ID. |
| `name` | body | `string` | no | Updated group name. |
