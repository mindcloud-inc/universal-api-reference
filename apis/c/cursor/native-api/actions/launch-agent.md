# Launch Agent with Cursor

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/agents`
- **Base URL:** `https://api.cursor.com`
- **Official documentation:** [Launch Agent](https://cursor.com/docs/cloud-agent/api/endpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt.text` | body | `string` | yes | Task or instructions for the agent to execute. |
| `source.repository` | body | `string` | no | GitHub repository URL for the agent to work in. Required unless using Source PR URL. |
| `source.ref` | body | `string` | no | Branch, tag, or commit hash to use as the base ref. |
| `model` | body | `string` | no | Explicit model ID from List Models, or `default` to use Cursor's configured default. |
| `target.autoCreatePr` | body | `boolean` | no | Whether Cursor should automatically create a pull request when the agent completes. |
| `target.branchName` | body | `string` | no | Custom branch name for the agent to create. |
| `source.prUrl` | body | `string` | no | GitHub pull request URL. When provided, Cursor works on the PR repository and branches. |
| `target.openAsCursorGithubApp` | body | `boolean` | no | Open the pull request as the Cursor GitHub App. Only applies when Auto Create PR is true. |
| `target.skipReviewerRequest` | body | `boolean` | no | Skip adding the user as reviewer when PR is opened by the Cursor GitHub App. |
| `target.autoBranch` | body | `boolean` | no | Whether to create a new branch when Source PR URL is provided. Defaults to true. |
| `webhook.url` | body | `string` | no | URL to receive agent status-change webhook notifications. |
| `webhook.secret` | body | `string` | no | Secret for webhook payload verification, minimum 32 characters. Maximum length: 256. |
| `prompt.images[]` | body | `array<object>` | no | Optional array of base64 encoded images, maximum 5. |
