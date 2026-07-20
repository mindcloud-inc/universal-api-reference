# Create Session with Browser Use

Creates a session or dispatches a task in Browser Use.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions`
- **Base URL:** `https://api.browser-use.com/api/v3`
- **Official documentation:** [Create Session](https://docs.browser-use.com/cloud/api-v3/sessions/create-session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentmail` | body | `boolean` | no | Whether to provision a temporary AgentMail inbox. |
| `cacheScript` | body | `boolean` | no | Controls deterministic script caching. |
| `enableRecording` | body | `boolean` | no | Whether to record the browser session. |
| `enableScheduledTasks` | body | `boolean` | no | Whether the agent may create scheduled tasks. |
| `keepAlive` | body | `boolean` | no | Keep the session idle after the task completes so follow-up tasks can reuse it. |
| `maxCostUsd` | body | `number` | no | Maximum allowed cost in USD for this session. |
| `model` | body | `string` | no | Model to use, such as claude-sonnet-4.6, gemini-3-flash, or claude-opus-4.6. |
| `outputSchema` | body | `object` | no | JSON Schema object for structured task output. |
| `profileId` | body | `string` | no | Browser profile ID to load into the session. |
| `proxyCountryCode` | body | `string` | no | Proxy country code such as us, de, or jp. Set null to disable proxy. |
| `sessionId` | body | `string` | no | Existing idle session ID to dispatch the task to. |
| `skills` | body | `boolean` | no | Whether to enable built-in Browser Use skills. |
| `task` | body | `string` | no | Natural-language instruction for the agent to execute. |
| `workspaceId` | body | `string` | no | Workspace ID to attach to the session. |
