# Find People with FindyMail

Finds people in FindyMail.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/search/employees`
- **Base URL:** `https://app.findymail.com`
- **Official documentation:** [Find People](https://www.findymail.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `website` | body | `string` | yes | Company website to search employees for, for example google.com. |
| `job_titles[]` | body | `array<string>` | yes | Job titles to match, for example CEO. |
| `count` | body | `number` | yes | Number of employee results to return. |
