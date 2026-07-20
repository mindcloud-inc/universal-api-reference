# Send Transactional Survey with Retently

Sends a transactional survey through Retently.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/survey`
- **Base URL:** `https://app.retently.com`
- **Official documentation:** [Send Transactional Survey](https://www.retently.com/api/#api-send-transactional-survey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign` | body | `string` | yes | The campaign ID where your customers will be surveyed |
| `delay` | body | `number` | no | Send the survey at a later day from the triggered event. The delay is counted in days (e.g., âdelayâ: 7); |
| `subscribers[]` | body | `array<string>` | yes | An array of objects that may contain 1 or up to 100 customers per request. Each customer object may include the following parameters: |
| `subscribers[].email` | body | `string` | yes | A variable with the email address of the customer |
| `subscribers[].firstName` | body | `string` | no | A variable with the first name of the customer |
| `subscribers[].lastName` | body | `string` | no | A variable with the last name of the customer |
| `subscribers[].company` | body | `string` | no | A variable with the company name of the customer |
| `subscribers[].tags[]` | body | `array<string>` | no | Any data passed in the array, will be imported as tags along with the customer. Example: [âfooâ, âbarâ, âbazâ] |
| `subscribers[].properties[]` | body | `array<object>` | no | Customer properties to send with the transactional survey. |
| `subscribers[].properties[].label` | body | `string` | yes | Property label |
| `subscribers[].properties[].type` | body | `string` | yes | Property type |
| `subscribers[].properties[].value` | body | `string` | yes | Property value |
