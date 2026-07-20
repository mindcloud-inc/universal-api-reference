# Update Policy with Clockify

Updates an existing policy in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/time-off/policies/:id`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Policy](https://docs.developer.clockify.me/#tag/Policy/operation/updatePolicy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `id` | path | `string<string>` | yes | — |
| `allowHalfDay` | body | `boolean` | yes | — |
| `allowNegativeBalance` | body | `boolean` | yes | — |
| `approve` | body | `object` | yes | — |
| `archived` | body | `boolean` | yes | — |
| `everyoneIncludingNew` | body | `boolean` | yes | — |
| `hasExpiration` | body | `boolean` | yes | — |
| `name` | body | `string` | yes | Maximum length: 100. |
| `userGroups` | body | `object` | yes | — |
| `users` | body | `object` | yes | — |
| `automaticAccrual` | body | `object` | no | — |
| `automaticTimeEntryCreation` | body | `object` | no | — |
| `color` | body | `string` | no | — |
| `icon` | body | `list<string>` | no | Accepted values: `CALENDAR`, `CHILDCARE`, `FAMILY`, `HEALTH_METRICS`, `LUGGAGE`, `MONETIZATION`, `PLANE`, `SNOWFLAKE`, `STETHOSCOPE`, `UMBRELLA`. |
| `negativeBalance` | body | `object` | no | — |
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
