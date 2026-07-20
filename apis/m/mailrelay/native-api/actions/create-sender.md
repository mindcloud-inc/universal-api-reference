# Create Sender with Mailrelay

Creates a new sender in Mailrelay.

## Endpoint

- **Method:** `POST`
- **Path:** `senders`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Create Sender](https://apidocs.mailrelay.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Sender email address. |
| `from_name` | body | `string` | no | Displayed sender name. |
| `name` | body | `string` | yes | Sender name. |
