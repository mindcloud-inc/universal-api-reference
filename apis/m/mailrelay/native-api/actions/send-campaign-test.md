# Send Campaign Test with Mailrelay

Sends a Mailrelay campaign to test email addresses.

## Endpoint

- **Method:** `POST`
- **Path:** `campaigns/:id/send_test`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Send Campaign Test](https://apidocs.mailrelay.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Mailrelay campaign ID. |
| `test_emails` | body | `string` | yes | Comma-separated email addresses for the campaign test send. |
