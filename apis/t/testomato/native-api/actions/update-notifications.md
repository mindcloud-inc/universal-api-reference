# Update notifications with Testomato

Updates project notification settings in Testomato.

## Endpoint

- **Method:** `POST`
- **Path:** `/project/:id/notifications`
- **Base URL:** `https://testomato.com/api`
- **Official documentation:** [Update notifications](https://help.testomato.com/api/update-notifications)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `severity` | body | `number` | no |
| `email` | body | `boolean` | no |
| `pagerduty` | body | `boolean` | no |
| `pushover` | body | `boolean` | no |
| `pushbullet` | body | `boolean` | no |
| `slack` | body | `boolean` | no |
| `webhook` | body | `boolean` | no |
