# Update Technician with ServiceTitan

## Endpoint

- **Method:** `PATCH`
- **Path:** `settings/v2/tenant/{tenant}/technicians/:id`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Update Technician](https://developer.servicetitan.io/docs/apis/tenant-settings-v2/endpoints/Technicians_Update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customFields[].typeId` | body | `number` | no | — |
| `id` | path | `number` | yes | ServiceTitan technician ID to update. |
| `customFields[].name` | body | `string` | no | — |
| `name` | body | `string` | no | Technician name. |
| `phoneNumber` | body | `string` | no | Technician phone number. |
| `email` | body | `string` | no | Technician email address. |
| `login` | body | `string` | no | Login username. |
| `businessUnitId` | body | `number` | no | Business unit ID. |
| `roleId` | body | `number` | no | User role ID. |
| `mainZoneId` | body | `number` | no | Main technician zone ID. |
| `zoneIds[]` | body | `array<number>` | no | All technician zone IDs. Sending this field replaces the existing zone list. |
| `projectLabelIds[]` | body | `array<number>` | no | Project label IDs. Sending this field replaces the existing list; it requires the Budget vs Actual feature flag. |
| `positions[]` | body | `array<string>` | no | Company positions. Allowed values: Installer, Service, Sales, Maintenance, Helper, InstallProductionManager, ServiceManager, SalesManager, PartRunner, DummyTech. |
| `aadUserId` | body | `string` | no | Azure Active Directory user ID. |
| `licenseType` | body | `list<string>` | no | Technician license type: NonManagedTech, ManagedTech, or ManagedInstaller. Accepted values: `ManagedInstaller`, `ManagedTech`, `NonManagedTech`. |
| `team` | body | `string` | no | Team name. |
| `dailyGoal` | body | `number` | no | Daily revenue goal. |
| `burdenRate` | body | `number` | no | Hourly burden rate. |
| `bio` | body | `string` | no | Technician biography; ServiceTitan accepts HTML. |
| `memo` | body | `string` | no | Technician memo; ServiceTitan accepts HTML. |
| `jobFilter` | body | `list<string>` | no | Upcoming appointment visibility setting. Accepted values: `AllScheduledDispatchedWorking`, `AllScheduledDispatchedWorkingFiveDays`, `AllScheduledDispatchedWorkingToday`, `AllScheduledDispatchedWorkingTodayTomorrow`, `DispatchedWorking`, `Next2ScheduledDispatchedWorkingToday`, `NextScheduledDispatchedWorking`, `NextScheduledDispatchedWorkingToday`, `NextScheduledDispatchedWorkingTodayTomorrow`. |
| `jobHistoryDateFilter` | body | `list<string>` | no | Appointment history visibility setting. Accepted values: `AllJobs`, `LastMonth`, `LastSevenDays`, `LastThreeDays`. |
| `home` | body | `object` | no | Home address object. When supplied, street and city are required. |
| `customFields[]` | body | `array<object>` | no | Technician custom-field entries, each with required typeId and optional value. |
| `accountLocked` | body | `boolean` | no | Whether the technician account is locked. |
| `customFields[].value` | body | `string` | no | — |
