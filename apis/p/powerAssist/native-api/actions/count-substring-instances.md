# Count Substring Instances with Power Assist

Counts substring matches with Power Assist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/string/countInstances`
- **Base URL:** `https://power-assist.p.rapidapi.com`
- **Official documentation:** [Count Substring Instances](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `string` | body | `string` | yes | The string to search within. |
| `substring` | body | `string` | yes | The substring to count. |
| `ignoreCase` | body | `boolean` | no | Whether matching should ignore letter case. |
