# Get Topic with Discourse

Retrieves a single topic from Discourse.

## Endpoint

- **Method:** `GET`
- **Path:** `/t/:id.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Get Topic](https://docs.discourse.org/#tag/Topics/operation/getTopic)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Numeric Discourse topic ID. |
