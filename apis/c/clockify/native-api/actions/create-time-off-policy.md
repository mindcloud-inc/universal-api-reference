# Create Time Off Policy with Clockify

Creates a time off policy in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/time-off/policies`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Create Time Off Policy](https://docs.developer.clockify.me/#tag/Policy/operation/createPolicy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `approve` | body | `object` | yes | — |
| `name` | body | `string` | yes | Maximum length: 100. |
| `allowHalfDay` | body | `boolean` | no | — |
| `allowNegativeBalance` | body | `boolean` | no | — |
| `archived` | body | `boolean` | no | — |
| `automaticAccrual` | body | `object` | no | — |
| `automaticTimeEntryCreation` | body | `object` | no | — |
| `color` | body | `string` | no | — |
| `everyoneIncludingNew` | body | `boolean` | no | — |
| `hasExpiration` | body | `boolean` | no | — |
| `icon` | body | `list<string>` | no | Accepted values: `CALENDAR`, `CHILDCARE`, `FAMILY`, `HEALTH_METRICS`, `LUGGAGE`, `MONETIZATION`, `PLANE`, `SNOWFLAKE`, `STETHOSCOPE`, `UMBRELLA`. |
| `negativeBalance` | body | `object` | no | — |
| `timeUnit` | body | `list<string>` | no | Accepted values: `DAYS`, `HOURS`. |
| `userGroups` | body | `object` | no | — |
| `users` | body | `object` | no | — |
| `approve.requiresApproval` | body | `boolean` | no | — |
| `approve.specificMembers` | body | `boolean` | no | — |
| `approve.teamManagers` | body | `boolean` | no | — |
| `approve.userIds[]` | body | `array<string>` | no | — |
| `automaticAccrual.amount` | body | `number` | yes | — |
| `automaticAccrual.period` | body | `string` | no | — |
| `automaticAccrual.timeUnit` | body | `string` | no | — |
| `automaticTimeEntryCreation.defaultEntities` | body | `object` | yes | — |
| `automaticTimeEntryCreation.defaultEntities.projectId` | body | `string` | no | — |
| `automaticTimeEntryCreation.defaultEntities.taskId` | body | `string` | no | — |
| `automaticTimeEntryCreation.enabled` | body | `boolean` | no | — |
| `negativeBalance.amount` | body | `number` | yes | — |
| `negativeBalance.amountValidForTimeUnit` | body | `boolean` | no | — |
| `negativeBalance.period` | body | `string` | no | — |
| `negativeBalance.shouldReset` | body | `boolean` | no | — |
| `negativeBalance.timeUnit` | body | `string` | no | — |
| `userGroups.contains` | body | `string` | no | — |
| `userGroups.ids[]` | body | `array<string>` | no | — |
| `userGroups.status` | body | `string` | no | — |
| `users.contains` | body | `string` | no | — |
| `users.ids[]` | body | `array<string>` | no | — |
| `users.status` | body | `string` | no | — |
