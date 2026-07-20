# List Calls with Retell AI

Retrieves calls from Retell AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/list-calls`
- **Base URL:** `https://api.retellai.com`
- **Official documentation:** [List Calls](https://docs.retellai.com/api-references/list-calls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter_criteria` | body | `object` | no | Filter criteria for the calls to retrieve. |
| `filter_criteria.agent_id[]` | body | `array<string>` | no | Only retrieve calls that are made with specific agent(s). |
| `filter_criteria.batch_call_id[]` | body | `array<string>` | no | Only retrieve calls with specific batch call id(s). |
| `filter_criteria.call_status[]` | body | `array<string>` | no | Only retrieve calls with specific call status(es). |
| `filter_criteria.call_successful[]` | body | `array<boolean>` | no | Only retrieve calls with specific call successful(s). |
| `filter_criteria.call_type[]` | body | `array<string>` | no | Only retrieve calls with specific call type(s). |
| `filter_criteria.direction[]` | body | `array<string>` | no | Only retrieve calls with specific direction(s). |
| `filter_criteria.disconnection_reason[]` | body | `array<string>` | no | Only retrieve calls with specific disconnection reason(s). |
| `filter_criteria.from_number[]` | body | `array<string>` | no | Only retrieve calls with specific from number(s). |
| `filter_criteria.in_voicemail[]` | body | `array<boolean>` | no | Only retrieve calls that are in voicemail or not in voicemail. |
| `filter_criteria.to_number[]` | body | `array<string>` | no | Only retrieve calls with specific to number(s). |
| `filter_criteria.user_sentiment[]` | body | `array<string>` | no | Only retrieve calls with specific user sentiment(s). |
| `filter_criteria.version[]` | body | `array<number>` | no | The version of the agent to use for the call. |
| `filter_criteria.agent_id[]` | body | `array<string>` | no | Only retrieve calls that are made with specific agent(s). |
| `filter_criteria.agent_id[]` | body | `array<string>` | no | Only retrieve calls that are made with specific agent(s). |
| `filter_criteria.version[]` | body | `array<number>` | no | The version of the agent to use for the call. |
| `filter_criteria.version[]` | body | `array<number>` | no | The version of the agent to use for the call. |
| `filter_criteria.call_status[]` | body | `array<string>` | no | Only retrieve calls with specific call status(es). |
| `filter_criteria.call_status[]` | body | `array<string>` | no | Only retrieve calls with specific call status(es). |
| `filter_criteria.in_voicemail[]` | body | `array<boolean>` | no | Only retrieve calls that are in voicemail or not in voicemail. |
| `filter_criteria.in_voicemail[]` | body | `array<boolean>` | no | Only retrieve calls that are in voicemail or not in voicemail. |
| `filter_criteria.disconnection_reason[]` | body | `array<string>` | no | Only retrieve calls with specific disconnection reason(s). |
| `filter_criteria.disconnection_reason[]` | body | `array<string>` | no | Only retrieve calls with specific disconnection reason(s). |
| `filter_criteria.from_number[]` | body | `array<string>` | no | Only retrieve calls with specific from number(s). |
| `filter_criteria.from_number[]` | body | `array<string>` | no | Only retrieve calls with specific from number(s). |
| `filter_criteria.to_number[]` | body | `array<string>` | no | Only retrieve calls with specific to number(s). |
| `filter_criteria.to_number[]` | body | `array<string>` | no | Only retrieve calls with specific to number(s). |
| `filter_criteria.batch_call_id[]` | body | `array<string>` | no | Only retrieve calls with specific batch call id(s). |
| `filter_criteria.batch_call_id[]` | body | `array<string>` | no | Only retrieve calls with specific batch call id(s). |
| `filter_criteria.call_type[]` | body | `array<string>` | no | Only retrieve calls with specific call type(s). |
| `filter_criteria.call_type[]` | body | `array<string>` | no | Only retrieve calls with specific call type(s). |
| `filter_criteria.direction[]` | body | `array<string>` | no | Only retrieve calls with specific direction(s). |
| `filter_criteria.direction[]` | body | `array<string>` | no | Only retrieve calls with specific direction(s). |
| `filter_criteria.user_sentiment[]` | body | `array<string>` | no | Only retrieve calls with specific user sentiment(s). |
| `filter_criteria.user_sentiment[]` | body | `array<string>` | no | Only retrieve calls with specific user sentiment(s). |
| `filter_criteria.call_successful[]` | body | `array<boolean>` | no | Only retrieve calls with specific call successful(s). |
| `filter_criteria.call_successful[]` | body | `array<boolean>` | no | Only retrieve calls with specific call successful(s). |
| `filter_criteria.start_timestamp` | body | `object` | no | Only retrieve calls with specific range of start timestamp(s). |
| `filter_criteria.start_timestamp.upper_threshold` | body | `number` | no | — |
| `filter_criteria.start_timestamp.lower_threshold` | body | `number` | no | — |
| `filter_criteria.end_timestamp` | body | `object` | no | Only retrieve calls with specific range of end timestamp(s). |
| `filter_criteria.end_timestamp.upper_threshold` | body | `number` | no | — |
| `filter_criteria.end_timestamp.lower_threshold` | body | `number` | no | — |
| `filter_criteria.duration_ms` | body | `object` | no | Only retrieve calls with specific range of duration(s). |
| `filter_criteria.duration_ms.upper_threshold` | body | `number` | no | — |
| `filter_criteria.duration_ms.lower_threshold` | body | `number` | no | — |
| `filter_criteria.e2e_latency_p50` | body | `object` | no | — |
| `filter_criteria.e2e_latency_p50.upper_threshold` | body | `number` | no | — |
| `filter_criteria.e2e_latency_p50.lower_threshold` | body | `number` | no | — |
| `filter_criteria.metadata` | body | `object` | no | Filter by metadata fields using dot notation (e.g., `metadata.customer_id`). Values are matched exactly as strings. |
| `filter_criteria.dynamic_variables` | body | `object` | no | Filter by dynamic variables using dot notation (e.g., `dynamic_variables.name`). Values are matched exactly as strings. |
| `sort_order` | body | `string` | no | The calls will be sorted by `start_timestamp`, whether to return the calls in ascending or descending order. Allowed values: ascending, descending. |
| `limit` | body | `number` | no | Limit the number of calls returned. Default 50, Max 1000. To retrieve more than 1000, use pagination_key to continue fetching the next page. |
| `pagination_key` | body | `string` | no | The pagination key to continue fetching the next page of calls. Pagination key is represented by a call id here, and it's exclusive (not included in the fetched calls). The last call id from the list calls is usually used as pagination key here. If not set, will start from the beginning. |
