# Cirra: Update Settings

Updates synced user settings in Cirra.

```
PUT https://connect.mindcloud.co/v1/universal/cirra/latest/actions/update-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cirra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cirra/latest/actions/update-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cirra/latest/actions/update-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `threadDetail` | list<string> | no | Choose how much command output to show in tasks. One of: `full_command_output`, `steps`, `steps_with_code_commands`. |
| `requireMetaEnterForLongPrompts` | boolean | no | Require the configured modifier before sending multi-line prompts. |
| `playThreadFinishSound` | boolean | no | Play a sound when a task finishes in another thread. |
| `theme` | list<string> | no | Choose the visual theme for Cirra. One of: `dark`, `light`, `system`. |
| `usePointerCursors` | boolean | no | Use pointer cursors for interactive UI elements. |
| `sansFontSizePx` | number | no | Primary interface font size in pixels. |
| `codeFontSizePx` | number | no | Code and terminal font size in pixels. |
| `personality` | list<string> | no | Choose a default tone for Cirra responses. One of: `friendly`, `pragmatic`. |
| `customInstructions` | string | no | Instructions that tailor Cirra to you. |
| `threadNamingPreferences` | string | no | Instructions for how AI should help name your tasks. |
| `enableCodeMode` | boolean | no | Turn on Cirra for developer workflows. |
| `allowProjectFolders` | boolean | no | Show non-Home project folders and project controls in the sidebar. |
| `enableTerminal` | boolean | no | Show terminal-specific controls inside code mode. |
| `allowAgentToUsePython` | boolean | no | Allow Cirra to use Python-based coding workflows. |
| `allowAgentToUseGit` | boolean | no | Allow Cirra to use Git-driven coding workflows. |
| `enableRemoteControl` | boolean | no | Let Cirra control your desktop from web tasks when you ask. |
| `allowLearnAboutYourJob` | boolean | no | Let Cirra remember your role, goals, and workflows. |
| `allowLearnAboutYourApps` | boolean | no | Let Cirra learn how you use connected apps. |
| `branchPrefix` | string | no | Prefix used when creating new branches in Cirra. |
| `alwaysForcePush` | boolean | no | Use force-with-lease when pushing from Cirra. |
| `commitInstructions` | string | no | Guidance appended to commit message generation prompts. |
| `pullRequestInstructions` | string | no | Guidance appended to pull request bodies created by Cirra. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowAgentToUseGit": true,
      "allowAgentToUsePython": true,
      "allowLearnAboutYourApps": true,
      "allowLearnAboutYourJob": true,
      "allowProjectFolders": true,
      "alwaysForcePush": true,
      "branchPrefix": "string",
      "codeFontSizePx": 1,
      "commitInstructions": "string",
      "customInstructions": "string",
      "enableCodeMode": true,
      "enableRemoteControl": true,
      "enableTerminal": true,
      "personality": "string",
      "playThreadFinishSound": true,
      "pullRequestInstructions": "string",
      "requireMetaEnterForLongPrompts": true,
      "sansFontSizePx": 1,
      "theme": "string",
      "threadDetail": "string",
      "threadNamingPreferences": "string",
      "usePointerCursors": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowAgentToUseGit` | boolean | Allow Cirra to use Git-driven coding workflows. |
| `allowAgentToUsePython` | boolean | Allow Cirra to use Python-based coding workflows. |
| `allowLearnAboutYourApps` | boolean | Let Cirra learn how you use connected apps. |
| `allowLearnAboutYourJob` | boolean | Let Cirra remember your role, goals, and workflows. |
| `allowProjectFolders` | boolean | Show non-Home project folders and project controls in the sidebar. |
| `alwaysForcePush` | boolean | Use force-with-lease when pushing from Cirra. |
| `branchPrefix` | string | Prefix used when creating new branches in Cirra. |
| `codeFontSizePx` | number | Code and terminal font size in pixels. |
| `commitInstructions` | string | Guidance appended to commit message generation prompts. |
| `customInstructions` | string | Instructions that tailor Cirra to you. |
| `enableCodeMode` | boolean | Turn on Cirra for developer workflows. |
| `enableRemoteControl` | boolean | Let Cirra control your desktop from web tasks when you ask. |
| `enableTerminal` | boolean | Show terminal-specific controls inside code mode. |
| `personality` | string | Choose a default tone for Cirra responses. |
| `playThreadFinishSound` | boolean | Play a sound when a task finishes in another thread. |
| `pullRequestInstructions` | string | Guidance appended to pull request bodies created by Cirra. |
| `requireMetaEnterForLongPrompts` | boolean | Require the configured modifier before sending multi-line prompts. |
| `sansFontSizePx` | number | Primary interface font size in pixels. |
| `theme` | string | Choose the visual theme for Cirra. |
| `threadDetail` | string | Choose how much command output to show in tasks. |
| `threadNamingPreferences` | string | Instructions for how AI should help name your tasks. |
| `usePointerCursors` | boolean | Use pointer cursors for interactive UI elements. |

## Native endpoint

Through the native Cirra API, this operation is `PUT /v1/cirra/settings` (base URL `http://api-public:9801`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-settings.md) for the provider-specific parameters and requirements.

