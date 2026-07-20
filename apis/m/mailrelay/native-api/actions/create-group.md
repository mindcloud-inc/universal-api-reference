# Create Group with Mailrelay

Creates a new subscriber group in Mailrelay.

## Endpoint

- **Method:** `POST`
- **Path:** `groups`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Create Group](https://apidocs.mailrelay.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Group description. |
| `name` | body | `string` | yes | Group name. |
