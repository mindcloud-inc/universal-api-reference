# Update Subscriber with SignalWire

Updates an existing subscriber in SignalWire.

## Endpoint

- **Method:** `PUT`
- **Path:** `/fabric/resources/subscribers/{id}`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Update Subscriber](https://signalwire.com/docs/apis/rest/subscribers/update-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of a Subscriber. |
| `password` | body | `string` | no | Password of the Subscriber. Defaults to a secure random password if not provided. |
| `email` | body | `string` | yes | Email of the Subscriber. |
| `first_name` | body | `string` | no | First name of the Subscriber. |
| `last_name` | body | `string` | no | Last name of the Subscriber. |
| `display_name` | body | `string` | no | Display name of the Subscriber. |
| `job_title` | body | `string` | no | Job title of the Subscriber. |
| `timezone` | body | `string` | no | Timezone of the Subscriber. |
| `country` | body | `string` | no | Country of the Subscriber. |
| `region` | body | `string` | no | Region of the Subscriber. |
| `company_name` | body | `string` | no | Company name of the Subscriber. |
