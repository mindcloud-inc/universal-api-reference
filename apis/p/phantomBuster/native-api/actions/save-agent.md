# Save Agent with PhantomBuster

Updates an agent in PhantomBuster.

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/save`
- **Base URL:** `https://api.phantombuster.com/api/v2`
- **Official documentation:** [Save Agent](https://hub.phantombuster.com/reference/post_agents-save)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentObject` | body | `string` | no | — |
| `applyScriptManifestDefaultSettings` | body | `boolean` | no | — |
| `argument` | body | `object` | no | — |
| `branch` | body | `string` | no | — |
| `day[]` | body | `array<number>` | no | — |
| `dow[]` | body | `array<string>` | no | — |
| `environment` | body | `list` | no | Accepted values: `release`, `staging`. |
| `executionTimeLimit` | body | `number` | no | — |
| `expireAt` | body | `number` | no | — |
| `fileMgmt` | body | `list` | no | Accepted values: `delete`, `folders`, `mix`. |
| `fileMgmtMaxFolders` | body | `number` | no | — |
| `groupSlug` | body | `string` | no | — |
| `hour[]` | body | `array<number>` | no | — |
| `id` | body | `string` | no | — |
| `idempotencyKey` | body | `string` | no | — |
| `isSimplePresetEnabled` | body | `boolean` | no | — |
| `launchAfterAgentId` | body | `string` | no | — |
| `launchOnceAt` | body | `number` | no | — |
| `launchType` | body | `list` | no | Accepted values: `after agent`, `manually`, `once`, `repeatedly`. |
| `location` | body | `string` | no | — |
| `mailAutomaticExitError` | body | `boolean` | no | — |
| `mailAutomaticExitSuccess` | body | `boolean` | no | — |
| `mailAutomaticLaunchError` | body | `boolean` | no | — |
| `mailAutomaticTimeError` | body | `boolean` | no | — |
| `mailManualExitError` | body | `boolean` | no | — |
| `mailManualExitSuccess` | body | `boolean` | no | — |
| `mailManualLaunchError` | body | `boolean` | no | — |
| `mailManualTimeError` | body | `boolean` | no | — |
| `masterAgentLaunchAfter` | body | `number` | no | — |
| `masterAgentLaunchOnExitCodes` | body | `string` | no | — |
| `maxParallelism` | body | `number` | no | — |
| `maxRetryNumber` | body | `number` | no | — |
| `minute[]` | body | `array<number>` | no | — |
| `month[]` | body | `array<string>` | no | — |
| `name` | body | `string` | no | — |
| `notifications` | body | `object` | no | — |
| `org` | body | `string` | no | — |
| `proxyAddress` | body | `string` | no | — |
| `proxyPassword` | body | `string` | no | — |
| `proxyType` | body | `list` | no | Accepted values: `http`, `none`, `pool`, `squid lease`. |
| `proxyUsername` | body | `string` | no | — |
| `refreshRate` | body | `number` | no | — |
| `repeatedLaunchPreset` | body | `list` | no | Accepted values: `4 times per day`, `4 times per hour`, `4 times per working hour`, `4 times per working hour, excluding weekends`, `6 times per day`, `8 times per day`, `Once every other day`, `Once every other hour`, `Once every other working hour`, `Once every other working hour, excluding weekends`, `Once per day`, `Once per day, at the start of the day`, `Once per hour`, `Once per working hour`, `Once per working hour, excluding weekends`, `Thrice per day`, `Thrice per hour`, `Thrice per working hour`, `Thrice per working hour, excluding weekends`, `Twice per day`, `Twice per hour`, `Twice per working hour`, `Twice per working hour, excluding weekends`. |
| `repeatedLaunchTimes` | body | `object` | no | — |
| `script` | body | `string` | no | — |
| `shouldPropagateUpdatedSettingsToWorkersRegardlessOfSessionType` | body | `boolean` | no | — |
| `simplePreset` | body | `list` | no | Accepted values: `4 times per day`, `4 times per hour`, `4 times per working hour`, `4 times per working hour, excluding weekends`, `6 times per day`, `8 times per day`, `Once every other day`, `Once every other hour`, `Once every other working hour`, `Once every other working hour, excluding weekends`, `Once per day`, `Once per day, at the start of the day`, `Once per hour`, `Once per working hour`, `Once per working hour, excluding weekends`, `Thrice per day`, `Thrice per hour`, `Thrice per working hour`, `Thrice per working hour, excluding weekends`, `Twice per day`, `Twice per hour`, `Twice per working hour`, `Twice per working hour, excluding weekends`. |
| `slackAutomaticExitError` | body | `boolean` | no | — |
| `slackAutomaticExitSuccess` | body | `boolean` | no | — |
| `slackAutomaticLaunchError` | body | `boolean` | no | — |
| `slackAutomaticTimeError` | body | `boolean` | no | — |
| `slackManualExitError` | body | `boolean` | no | — |
| `slackManualExitSuccess` | body | `boolean` | no | — |
| `slackManualLaunchError` | body | `boolean` | no | — |
| `slackManualTimeError` | body | `boolean` | no | — |
| `slackWebHook` | body | `string` | no | — |
| `squidLeaseIdentifier` | body | `object` | no | — |
| `sublocation` | body | `string` | no | — |
| `timezone` | body | `string` | no | — |
| `wasSetupValidWhenSubmittedByTheFrontend` | body | `boolean` | no | — |
| `webhook` | body | `string` | no | — |
