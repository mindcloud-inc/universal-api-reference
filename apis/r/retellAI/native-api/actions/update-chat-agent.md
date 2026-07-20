# Update Chat Agent with Retell AI

Updates a chat agent in Retell AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/update-chat-agent/{agent_id}`
- **Base URL:** `https://api.retellai.com`
- **Official documentation:** [Update Chat Agent](https://docs.retellai.com/api-references/update-chat-agent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | — |
| `guardrail_config.input_topics[]` | body | `array<string>` | no | Selected prohibited user topic categories to check. When user messages contain these topics, the agent will respond with a placeholder message instead of processing the request. |
| `guardrail_config.output_topics[]` | body | `array<string>` | no | Selected prohibited agent topic categories to check. When agent messages contain these topics, they will be replaced with a placeholder message. |
| `pii_config.categories[]` | body | `array<string>` | yes | List of PII categories to scrub from transcripts and recordings. |
| `post_chat_analysis_data[]` | body | `array<object>` | no | Post chat analysis data to extract from the chat. This data will augment the pre-defined variables extracted in the chat analysis. This will be available after the chat ends. |
| `post_chat_analysis_data[].examples[]` | body | `array<string>` | no | Examples of the variable value to teach model the style and syntax. |
| `webhook_events[]` | body | `array<string>` | no | Which webhook events this agent should receive. If not set, defaults to chat_started, chat_ended, chat_analyzed. |
| `version` | query | `number` | no | — |
| `response_engine` | body | `object` | no | — |
| `response_engine.type` | body | `string` | yes | type of the Response Engine. Allowed values: retell-llm. |
| `response_engine.llm_id` | body | `string` | yes | id of the Retell LLM Response Engine. |
| `response_engine.version` | body | `number` | no | Version of the Retell LLM Response Engine. |
| `agent_name` | body | `string` | no | The name of the chat agent. Only used for your own reference. |
| `auto_close_message` | body | `string` | no | Message to display when the chat is automatically closed. |
| `end_chat_after_silence_ms` | body | `number` | no | If users stay silent for a period after agent speech, end the chat. The minimum value allowed is 120,000 ms (2 minutes). The maximum value allowed is 259,200,000 ms (72 hours). By default, this is set to 3,600,000 (1 hour). |
| `language` | body | `string` | no | Specifies what language (and dialect) the chat will operate in. For instance, selecting `en-GB` optimizes for British English. If unset, will use default value `en-US`. Select `multi` for multilingual support, currently this supports Spanish and English. |
| `webhook_url` | body | `string` | no | The webhook for agent to listen to chat events. See what events it would get at [webhook doc](/features/webhook). If set, will binds webhook events for this agent to the specified url, and will ignore the account level webhook for this agent. Set to `null` to remove webhook url from this agent. |
| `webhook_events[]` | body | `array<string>` | no | Which webhook events this agent should receive. If not set, defaults to chat_started, chat_ended, chat_analyzed. |
| `webhook_events[]` | body | `array<string>` | no | Which webhook events this agent should receive. If not set, defaults to chat_started, chat_ended, chat_analyzed. |
| `webhook_timeout_ms` | body | `number` | no | The timeout for the webhook in milliseconds. If not set, default value of 10000 will apply. |
| `data_storage_setting` | body | `string` | no | Controls what data is stored for this agent. "everything" stores all data including transcripts and recordings. "everything_except_pii" stores data but excludes PII when possible based on PII configuration. "basic_attributes_only" stores only basic metadata. If not set, defaults to "everything". Allowed values: everything, everything_except_pii, basic_attributes_only. |
| `data_storage_retention_days` | body | `number` | no | Number of days to retain call/chat data before automatic deletion. Must be between 1 and 730 days. If not set, data is retained forever (no automatic deletion). |
| `opt_in_signed_url` | body | `boolean` | no | Whether this agent opts in to signed url for public log. If not set, default value of false will apply. |
| `signed_url_expiration_ms` | body | `number` | no | The expiration time for the signed url in milliseconds. Only applicable when opt_in_signed_url is true. If not set, default value of 86400000 (24 hours) will apply. |
| `post_chat_analysis_data[]` | body | `array<object>` | no | Post chat analysis data to extract from the chat. This data will augment the pre-defined variables extracted in the chat analysis. This will be available after the chat ends. |
| `post_chat_analysis_data[]` | body | `array<object>` | no | Post chat analysis data to extract from the chat. This data will augment the pre-defined variables extracted in the chat analysis. This will be available after the chat ends. |
| `post_chat_analysis_data[].type` | body | `string` | yes | Type of the variable to extract. Allowed values: string. |
| `post_chat_analysis_data[].name` | body | `string` | yes | Name of the variable. |
| `post_chat_analysis_data[].description` | body | `string` | yes | Description of the variable. |
| `post_chat_analysis_data[].examples[]` | body | `array<string>` | no | Examples of the variable value to teach model the style and syntax. |
| `post_chat_analysis_data[].examples[]` | body | `array<string>` | no | Examples of the variable value to teach model the style and syntax. |
| `post_chat_analysis_data[].required` | body | `boolean` | no | Whether this data is required. If true and the data is not extracted, the call will be marked as unsuccessful. |
| `post_chat_analysis_model` | body | `string` | no | Available LLM models for agents. |
| `analysis_successful_prompt` | body | `string` | no | The prompt to use for post call analysis to evaluate whether the call is successful. Set to null to use the default prompt. |
| `analysis_summary_prompt` | body | `string` | no | The prompt to use for post call analysis to summarize the call. Set to null to use the default prompt. |
| `analysis_user_sentiment_prompt` | body | `string` | no | Prompt to guide how the post chat analysis should evaluate user sentiment. When unset, the default system prompt is used. Set to null to use the default prompt. |
| `pii_config` | body | `object` | no | — |
| `pii_config.mode` | body | `string` | yes | The processing mode for PII scrubbing. Currently only post-call is supported. Allowed values: post_call. |
| `pii_config.categories[]` | body | `array<string>` | yes | List of PII categories to scrub from transcripts and recordings. |
| `pii_config.categories[]` | body | `array<string>` | yes | List of PII categories to scrub from transcripts and recordings. |
| `guardrail_config` | body | `object` | no | — |
| `guardrail_config.output_topics[]` | body | `array<string>` | no | Selected prohibited agent topic categories to check. When agent messages contain these topics, they will be replaced with a placeholder message. |
| `guardrail_config.output_topics[]` | body | `array<string>` | no | Selected prohibited agent topic categories to check. When agent messages contain these topics, they will be replaced with a placeholder message. |
| `guardrail_config.input_topics[]` | body | `array<string>` | no | Selected prohibited user topic categories to check. When user messages contain these topics, the agent will respond with a placeholder message instead of processing the request. |
| `guardrail_config.input_topics[]` | body | `array<string>` | no | Selected prohibited user topic categories to check. When user messages contain these topics, the agent will respond with a placeholder message instead of processing the request. |
| `is_public` | body | `boolean` | no | Whether the agent is public. When set to true, the agent is available for public agent preview link. |
