# Retrieve Message Responses with boomApp Connect

Retrieves responses to outbound messages from boomApp Connect.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/get_responses`
- **Base URL:** `https://direct-api.apps.boomcomms.com`
- **Official documentation:** [Retrieve Message Responses](https://github.com/microsoft/PowerPlatformConnectors/blob/dev/certified-connectors/BoomappConnect/apiDefinition.swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `unique_identifier` | query | `string` | no | Return responses for outbound messages with this unique_identifier. |
| `custom_parameter` | query | `string` | no | Return responses for outbound messages with this custom_parameter. |
| `campaign_name` | query | `string` | no | Return responses for outbound messages with this campaign_name. |
| `transaction_id` | query | `string` | no | Return responses for this outbound transaction ID. |
| `ignore_previous` | query | `boolean` | no | Exclude previously retrieved responses. |
| `mark_as_read` | query | `boolean` | no | Mark retrieved responses as read. |
| `conversationId` | query | `string` | no | Return responses for a conversation thread. |
