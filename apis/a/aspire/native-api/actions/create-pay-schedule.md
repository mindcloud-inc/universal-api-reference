# Create Pay Schedule with Aspire

## Endpoint

- **Method:** `POST`
- **Path:** `PaySchedules`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Pay Schedule](https://guide.youraspire.com/apidocs/payschedules-3)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `active` | body | `boolean` | yes |
| `dailyHoursBeforeOt` | body | `number` | yes |
| `weeklyHoursBeforeOt` | body | `number` | yes |
| `payScheduleName` | body | `string` | yes |
| `defaultOtPayCodeId` | body | `list<number>` | yes |
| `defaultPayCodeId` | body | `list<number>` | yes |
