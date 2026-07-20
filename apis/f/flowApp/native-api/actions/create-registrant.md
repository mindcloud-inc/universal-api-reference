# Create Registrant with Flow App

## Endpoint

- **Method:** `POST`
- **Path:** `/registrants`
- **Base URL:** `https://prod.flowapp.com/api/v1`
- **Official documentation:** [Create Registrant](https://support.flowapp.com/support/solutions/articles/12000076814-flow-api-0-0-4)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The attendee email address to register. |
| `firstName` | body | `string` | yes | The attendee first name. |
| `lastName` | body | `string` | yes | The attendee last name. |
| `eventSessionToken` | body | `string` | yes | The target event session token. |
| `redirect` | body | `boolean` | no | Optional SSO-style redirect flag documented by Flow. |
