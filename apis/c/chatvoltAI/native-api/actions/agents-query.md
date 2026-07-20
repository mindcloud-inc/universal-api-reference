# Agent Query with Chatvolt AI

Sends a query to an agent in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/{id}/query`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Agent Query](https://docs.chatvolt.ai/api-reference/endpoint/agents/query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the agent to be queried. |
| `query` | body | `string` | yes | Text of the question or command to be sent to the agent. |
| `streaming` | body | `boolean` | no | Set to `true` to receive a Server-Sent Events (SSE) stream, `false` for a single JSON response. |
| `conversationId` | body | `string` | no | ID of the existing conversation. If not provided or invalid, a new conversation will be created. |
| `contactId` | body | `string` | no | ID of an existing contact in the system. If provided, associates the conversation with this contact. Alternative to the `contact` object. |
| `contact` | body | `object` | no | Contact details. Used to find an existing contact (by email, phoneNumber, or userId) or create a new one if not found. |
| `visitorId` | body | `string` | no | ID of the visitor/participant who is sending the query. If not provided, a new ID will be generated. |
| `temperature` | body | `number` | no | Model temperature (min 0.0, max 1.0). Controls the randomness of the response. |
| `modelName` | body | `string` | no | Allows overriding the LLM model configured in the agent for this specific query. Use [valid model names](https://api.chatvolt.ai/agents/models). |
| `presencePenalty` | body | `number` | no | Presence penalty (between -2.0 and 2.0). Positive values encourage the model to talk about new topics. |
| `frequencyPenalty` | body | `number` | no | Frequency penalty (between -2.0 and 2.0). Positive values discourage the model from repeating textual lines. |
| `topP` | body | `number` | no | Nucleus sampling (alternative to temperature). Considers tokens with accumulated probability mass top_p. (Ex: 0.1 considers the top 10%). It is recommended to change `topP` or `temperature`, not both. |
| `filters` | body | `object` | no | Filters for application/json requests. |
| `systemPrompt` | body | `string` | no | Allows overriding the system prompt configured in the agent for this specific query. |
| `context` | body | `object` | no | Object to pass additional context data that can be used by tools or in the prompt. |
| `callbackURL` | body | `string` | no | Optional URL. If provided, the API will return 202 immediately and will deliver the response to the Agent via a POST request to this URL when it is ready. |
