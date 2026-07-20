# Initiate Individual Call with Ringg AI

Initiates an individual outbound call in Ringg AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/calling/outbound/individual`
- **Base URL:** `https://prod-api.ringg.ai/ca/api/v0`
- **Official documentation:** [Initiate Individual Call](https://docs.ringg.ai/api-reference/endpoint/calling/initiate-individual-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the person to call |
| `mobile_number` | body | `string` | yes | The phone number to call (must include country code, e.g., +91 for India) |
| `agent_id` | body | `string` | yes | UUID of the agent that will handle the call |
| `from_number` | body | `string` | yes | The phone number to call from (with country code) |
| `custom_args_values` | body | `object` | no | Custom variables that will be replaced in the agent's prompt using @{{variable_name}} syntax |
| `custom_args_values.company_name` | body | `string` | no | Company name for context |
| `custom_args_values.appointment_date` | body | `string` | no | Appointment date |
| `custom_args_values.product_name` | body | `string` | no | Product name for sales calls |
| `smart_formatter` | body | `object` | no | (Optional) Smart formatting for callee name — supports first name extraction and dictionary-based transliteration |
| `smart_formatter.extract_first_name` | body | `boolean` | no | Extract the first actual name from the full name, skipping common prefixes (Mr, Mrs, Dr, etc.) |
| `smart_formatter.transliteration` | body | `boolean` | no | Transliterate the extracted name to the target language using a local dictionary. When enabled, extract_first_name is automatically applied. |
| `smart_formatter.transliteration_language` | body | `object` | no | Language configuration for transliteration |
| `smart_formatter.transliteration_language.source` | body | `string` | no | Source language code (default: en) |
| `smart_formatter.transliteration_language.target` | body | `string` | no | Target language code (default: hi) |
| `call_config` | body | `object` | no | (Optional) Override default call configuration |
| `call_config.idle_timeout_warning` | body | `number` | no | Seconds before idle warning (default: 5) |
| `call_config.idle_timeout_end` | body | `number` | no | Seconds before call termination (default: 10) |
| `call_config.max_call_length` | body | `number` | no | Maximum call duration in seconds (default: 240) |
| `call_config.call_retry_config` | body | `object` | no | Retry configuration for failed calls |
| `call_config.call_retry_config.retry_count` | body | `number` | no | Number of retry attempts |
| `call_config.call_retry_config.retry_busy` | body | `number` | no | Minutes to wait if busy (default: 30) |
| `call_config.call_retry_config.retry_not_picked` | body | `number` | no | Minutes to wait if not picked (default: 30) |
| `call_config.call_retry_config.retry_failed` | body | `number` | no | Minutes to wait if failed (default: 30) |
| `call_config.call_time` | body | `object` | no | Time window configuration for calls |
| `call_config.call_time.call_start_time` | body | `string` | no | When calls can start (default: 00:00) |
| `call_config.call_time.call_end_time` | body | `string` | no | When calls must end (default: 23:00) |
| `call_config.call_time.timezone` | body | `string` | no | Timezone for call times (default: Asia/Kolkata) |
