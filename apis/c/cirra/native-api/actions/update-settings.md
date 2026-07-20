# Update Settings with Cirra

Updates synced user settings in Cirra.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/cirra/settings`
- **Base URL:** `http://api-public:9801`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `threadDetail` | body | `list<string>` | no | Choose how much command output to show in tasks. Accepted values: `full_command_output`, `steps`, `steps_with_code_commands`. |
| `requireMetaEnterForLongPrompts` | body | `boolean` | no | Require the configured modifier before sending multi-line prompts. |
| `playThreadFinishSound` | body | `boolean` | no | Play a sound when a task finishes in another thread. |
| `theme` | body | `list<string>` | no | Choose the visual theme for Cirra. Accepted values: `dark`, `light`, `system`. |
| `usePointerCursors` | body | `boolean` | no | Use pointer cursors for interactive UI elements. |
| `sansFontSizePx` | body | `number` | no | Primary interface font size in pixels. |
| `codeFontSizePx` | body | `number` | no | Code and terminal font size in pixels. |
| `personality` | body | `list<string>` | no | Choose a default tone for Cirra responses. Accepted values: `friendly`, `pragmatic`. |
| `customInstructions` | body | `string` | no | Instructions that tailor Cirra to you. |
| `threadNamingPreferences` | body | `string` | no | Instructions for how AI should help name your tasks. |
| `enableCodeMode` | body | `boolean` | no | Turn on Cirra for developer workflows. |
| `allowProjectFolders` | body | `boolean` | no | Show non-Home project folders and project controls in the sidebar. |
| `enableTerminal` | body | `boolean` | no | Show terminal-specific controls inside code mode. |
| `allowAgentToUsePython` | body | `boolean` | no | Allow Cirra to use Python-based coding workflows. |
| `allowAgentToUseGit` | body | `boolean` | no | Allow Cirra to use Git-driven coding workflows. |
| `enableRemoteControl` | body | `boolean` | no | Let Cirra control your desktop from web tasks when you ask. |
| `allowLearnAboutYourJob` | body | `boolean` | no | Let Cirra remember your role, goals, and workflows. |
| `allowLearnAboutYourApps` | body | `boolean` | no | Let Cirra learn how you use connected apps. |
| `branchPrefix` | body | `string` | no | Prefix used when creating new branches in Cirra. |
| `alwaysForcePush` | body | `boolean` | no | Use force-with-lease when pushing from Cirra. |
| `commitInstructions` | body | `string` | no | Guidance appended to commit message generation prompts. |
| `pullRequestInstructions` | body | `string` | no | Guidance appended to pull request bodies created by Cirra. |
