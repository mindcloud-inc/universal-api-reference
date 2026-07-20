# Create Subscriber Token with SignalWire

Creates a new subscriber token in SignalWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/fabric/subscribers/tokens`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Create Subscriber Token](https://signalwire.com/docs/apis/rest/subscribers/tokens/create-subscriber-token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reference` | body | `string` | yes | A string that uniquely identifies the subscriber. Often it's an email, but can be any other string. |
| `expire_at` | body | `number` | no | A unixtime (the number of seconds since 1970-01-01 00:00:00) at which the token should no longer be valid. Defaults to 'two hours from now' |
| `application_id` | body | `string` | no | The ID of the application that the token is associated with. |
| `password` | body | `string` | no | Set or update the subscriber's password. Omit this field or pass an empty string if you don't want to update the password. |
| `first_name` | body | `string` | no | Set or update the first name of the subscriber. |
| `last_name` | body | `string` | no | Set or update the last name of the subscriber. |
| `display_name` | body | `string` | no | Set or update the display name of the subscriber. |
| `job_title` | body | `string` | no | Set or update the job title of the subscriber. |
| `time_zone` | body | `string` | no | Set or update the time zone of the subscriber. |
| `country` | body | `string` | no | Set or update the country of the subscriber. |
| `region` | body | `string` | no | Set or update the region of the subscriber. |
| `company_name` | body | `string` | no | Set or update the company name of the subscriber. |
