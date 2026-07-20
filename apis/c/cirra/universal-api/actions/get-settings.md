# Cirra: Get Settings

Retrieves synced user settings from Cirra.

```
GET https://connect.mindcloud.co/v1/universal/cirra/latest/actions/get-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cirra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cirra/latest/actions/get-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cirra/latest/actions/get-settings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Cirra API, this operation is `GET /v1/cirra/settings` (base URL `http://api-public:9801`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-settings.md) for the provider-specific parameters and requirements.

