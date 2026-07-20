# PhantomBuster: Save Agent

Updates an agent in PhantomBuster.

```
PUT https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/save-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhantomBuster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/save-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/save-agent', {
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
| `agentObject` | string | no |  |
| `applyScriptManifestDefaultSettings` | boolean | no |  |
| `argument` | object | no |  |
| `branch` | string | no |  |
| `environment` | list | no | One of: `release`, `staging`. |
| `executionTimeLimit` | number | no |  |
| `expireAt` | number | no |  |
| `fileMgmt` | list | no | One of: `delete`, `folders`, `mix`. |
| `fileMgmtMaxFolders` | number | no |  |
| `id` | string | no |  |
| `idempotencyKey` | string | no |  |
| `launchAfterAgentId` | string | no |  |
| `launchOnceAt` | number | no |  |
| `launchType` | list | no | One of: `after agent`, `manually`, `once`, `repeatedly`. |
| `masterAgentLaunchAfter` | number | no |  |
| `masterAgentLaunchOnExitCodes` | string | no |  |
| `maxParallelism` | number | no |  |
| `maxRetryNumber` | number | no |  |
| `name` | string | no |  |
| `notifications` | object | no |  |
| `notifications.mailAutomaticExitError` | boolean | no |  |
| `notifications.mailAutomaticExitSuccess` | boolean | no |  |
| `notifications.mailAutomaticLaunchError` | boolean | no |  |
| `notifications.mailAutomaticTimeError` | boolean | no |  |
| `notifications.mailManualExitError` | boolean | no |  |
| `notifications.mailManualExitSuccess` | boolean | no |  |
| `notifications.mailManualLaunchError` | boolean | no |  |
| `notifications.mailManualTimeError` | boolean | no |  |
| `notifications.slackAutomaticExitError` | boolean | no |  |
| `notifications.slackAutomaticExitSuccess` | boolean | no |  |
| `notifications.slackAutomaticLaunchError` | boolean | no |  |
| `notifications.slackAutomaticTimeError` | boolean | no |  |
| `notifications.slackManualExitError` | boolean | no |  |
| `notifications.slackManualExitSuccess` | boolean | no |  |
| `notifications.slackManualLaunchError` | boolean | no |  |
| `notifications.slackManualTimeError` | boolean | no |  |
| `notifications.slackWebHook` | string | no |  |
| `notifications.webhook` | string | no |  |
| `org` | string | no |  |
| `proxyAddress` | string | no |  |
| `proxyPassword` | string | no |  |
| `proxyType` | list | no | One of: `http`, `none`, `pool`, `squid lease`. |
| `proxyUsername` | string | no |  |
| `repeatedLaunchPreset` | list | no | One of: `4 times per day`, `4 times per hour`, `4 times per working hour`, `4 times per working hour, excluding weekends`, `6 times per day`, `8 times per day`, `Once every other day`, `Once every other hour`, `Once every other working hour`, `Once every other working hour, excluding weekends`, `Once per day`, `Once per day, at the start of the day`, `Once per hour`, `Once per working hour`, `Once per working hour, excluding weekends`, `Thrice per day`, `Thrice per hour`, `Thrice per working hour`, `Thrice per working hour, excluding weekends`, `Twice per day`, `Twice per hour`, `Twice per working hour`, `Twice per working hour, excluding weekends`. |
| `repeatedLaunchTimes` | object | no |  |
| `repeatedLaunchTimes.day[]` | array<number> | no |  |
| `repeatedLaunchTimes.dow[]` | array<string> | no |  |
| `repeatedLaunchTimes.hour[]` | array<number> | no |  |
| `repeatedLaunchTimes.isSimplePresetEnabled` | boolean | no |  |
| `repeatedLaunchTimes.minute[]` | array<number> | no |  |
| `repeatedLaunchTimes.month[]` | array<string> | no |  |
| `repeatedLaunchTimes.simplePreset` | list | no | One of: `4 times per day`, `4 times per hour`, `4 times per working hour`, `4 times per working hour, excluding weekends`, `6 times per day`, `8 times per day`, `Once every other day`, `Once every other hour`, `Once every other working hour`, `Once every other working hour, excluding weekends`, `Once per day`, `Once per day, at the start of the day`, `Once per hour`, `Once per working hour`, `Once per working hour, excluding weekends`, `Thrice per day`, `Thrice per hour`, `Thrice per working hour`, `Thrice per working hour, excluding weekends`, `Twice per day`, `Twice per hour`, `Twice per working hour`, `Twice per working hour, excluding weekends`. |
| `repeatedLaunchTimes.timezone` | string | no |  |
| `script` | string | no |  |
| `shouldPropagateUpdatedSettingsToWorkersRegardlessOfSessionType` | boolean | no |  |
| `squidLeaseIdentifier` | object | no |  |
| `squidLeaseIdentifier.groupSlug` | string | no |  |
| `squidLeaseIdentifier.location` | string | no |  |
| `squidLeaseIdentifier.refreshRate` | number | no |  |
| `squidLeaseIdentifier.sublocation` | string | no |  |
| `wasSetupValidWhenSubmittedByTheFrontend` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PhantomBuster API returns.

## Native endpoint

Through the native PhantomBuster API, this operation is `POST /agents/save` (base URL `https://api.phantombuster.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-agent.md) for the provider-specific parameters and requirements.

