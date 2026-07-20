# Get Stats Summary with Mailrelay

Retrieves account stats summary from Mailrelay.

## Endpoint

- **Method:** `GET`
- **Path:** `stats`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Get Stats Summary](https://apidocs.mailrelay.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_time` | query | `string` | yes | End time in `YYYY-MM-DD HH:MM:SS` format. |
| `start_time` | query | `string` | yes | Start time in `YYYY-MM-DD HH:MM:SS` format. |
