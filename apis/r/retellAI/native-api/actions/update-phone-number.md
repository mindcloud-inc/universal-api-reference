# Update Phone Number with Retell AI

Updates a phone number in Retell AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/update-phone-number/{phone_number}`
- **Base URL:** `https://api.retellai.com`
- **Official documentation:** [Update Phone Number](https://docs.retellai.com/api-references/update-phone-number)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allowed_inbound_country_list[]` | body | `array<string>` | no | List of ISO 3166-1 alpha-2 country codes from which inbound calls are allowed. If not set or empty, calls from all countries are allowed. |
| `allowed_outbound_country_list[]` | body | `array<string>` | no | List of ISO 3166-1 alpha-2 country codes to which outbound calls are allowed. If not set or empty, calls to all countries are allowed. |
| `inbound_agents[]` | body | `array<object>` | no | Inbound agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each inbound call, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to inbound_agent_id. |
| `inbound_sms_agents[]` | body | `array<object>` | no | Inbound SMS agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each inbound SMS, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to inbound_sms_agent_id. |
| `outbound_agents[]` | body | `array<object>` | no | Outbound agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each outbound call, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to outbound_agent_id. |
| `outbound_sms_agents[]` | body | `array<object>` | no | Outbound SMS agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each outbound SMS, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to outbound_sms_agent_id. |
| `phone_number` | path | `string` | yes | — |
| `inbound_agent_id` | body | `string` | no | Unique id of agent to bind to the number. The number will automatically use the agent when receiving inbound calls. If set to null, this number would not accept inbound call. Deprecated. See https://docs.retellai.com/deprecation-notice/2026/03-31_phone_number_agent_fields |
| `outbound_agent_id` | body | `string` | no | Unique id of agent to bind to the number. The number will automatically use the agent when conducting outbound calls. If set to null, this number would not be able to initiate outbound call without agent id override. Deprecated. See https://docs.retellai.com/deprecation-notice/2026/03-31_phone_number_agent_fields |
| `inbound_agent_version` | body | `number` | no | Version of the inbound agent to bind to the number. If not provided, will default to latest version. Deprecated. See https://docs.retellai.com/deprecation-notice/2026/03-31_phone_number_agent_fields |
| `outbound_agent_version` | body | `number` | no | Version of the outbound agent to bind to the number. If not provided, will default to latest version. |
| `inbound_agents[]` | body | `array<object>` | no | Inbound agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each inbound call, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to inbound_agent_id. |
| `inbound_agents[]` | body | `array<object>` | no | Inbound agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each inbound call, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to inbound_agent_id. |
| `inbound_agents[].agent_id` | body | `string` | yes | — |
| `inbound_agents[].agent_version` | body | `number` | no | — |
| `inbound_agents[].weight` | body | `number` | yes | The weight of the agent. When used in a list of agents, the total weights must add up to 1. |
| `outbound_agents[]` | body | `array<object>` | no | Outbound agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each outbound call, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to outbound_agent_id. |
| `outbound_agents[]` | body | `array<object>` | no | Outbound agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each outbound call, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to outbound_agent_id. |
| `outbound_agents[].agent_id` | body | `string` | yes | — |
| `outbound_agents[].agent_version` | body | `number` | no | — |
| `outbound_agents[].weight` | body | `number` | yes | The weight of the agent. When used in a list of agents, the total weights must add up to 1. |
| `inbound_sms_agents[]` | body | `array<object>` | no | Inbound SMS agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each inbound SMS, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to inbound_sms_agent_id. |
| `inbound_sms_agents[]` | body | `array<object>` | no | Inbound SMS agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each inbound SMS, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to inbound_sms_agent_id. |
| `inbound_sms_agents[].agent_id` | body | `string` | yes | — |
| `inbound_sms_agents[].agent_version` | body | `number` | no | — |
| `inbound_sms_agents[].weight` | body | `number` | yes | The weight of the agent. When used in a list of agents, the total weights must add up to 1. |
| `outbound_sms_agents[]` | body | `array<object>` | no | Outbound SMS agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each outbound SMS, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to outbound_sms_agent_id. |
| `outbound_sms_agents[]` | body | `array<object>` | no | Outbound SMS agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each outbound SMS, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to outbound_sms_agent_id. |
| `outbound_sms_agents[].agent_id` | body | `string` | yes | — |
| `outbound_sms_agents[].agent_version` | body | `number` | no | — |
| `outbound_sms_agents[].weight` | body | `number` | yes | The weight of the agent. When used in a list of agents, the total weights must add up to 1. |
| `nickname` | body | `string` | no | Nickname of the number. This is for your reference only. |
| `inbound_webhook_url` | body | `string` | no | If set, will send a webhook for inbound calls, where you can to override agent id, set dynamic variables and other fields specific to that call. |
| `inbound_sms_webhook_url` | body | `string` | no | If set, will send a webhook for inbound SMS, where you can override agent id, set dynamic variables and other fields specific to that chat. |
| `allowed_inbound_country_list[]` | body | `array<string>` | no | List of ISO 3166-1 alpha-2 country codes from which inbound calls are allowed. If not set or empty, calls from all countries are allowed. |
| `allowed_inbound_country_list[]` | body | `array<string>` | no | List of ISO 3166-1 alpha-2 country codes from which inbound calls are allowed. If not set or empty, calls from all countries are allowed. |
| `allowed_outbound_country_list[]` | body | `array<string>` | no | List of ISO 3166-1 alpha-2 country codes to which outbound calls are allowed. If not set or empty, calls to all countries are allowed. |
| `allowed_outbound_country_list[]` | body | `array<string>` | no | List of ISO 3166-1 alpha-2 country codes to which outbound calls are allowed. If not set or empty, calls to all countries are allowed. |
| `termination_uri` | body | `string` | no | The termination uri to update for the phone number. This is used for outbound calls. |
| `auth_username` | body | `string` | no | The username used for authentication for the SIP trunk to update for the phone number. |
| `auth_password` | body | `string` | no | The password used for authentication for the SIP trunk to update for the phone number. |
| `transport` | body | `string` | no | Outbound transport protocol to update for the phone number. Valid values are "TLS", "TCP" and "UDP". Default is "TCP". |
| `fallback_number` | body | `string` | no | Enterprise only. Phone number to transfer inbound calls to when organization is in outage mode. Can be either a Retell phone number or an external number. Set to null to remove. Cannot be the same as this phone number, and cannot be a number that already has its own fallback configured (prevents nested forwarding). |
