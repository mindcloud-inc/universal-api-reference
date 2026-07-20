# Helper Functions - Get Current Time in Timezone with Pipedream Utils

Retrieves the current time in a timezone in Pipedream Utils.

## Endpoint

- **Method:** `GET`
- **Base URL:** `https://pipedream.com`
- **Official documentation:** [Helper Functions - Get Current Time in Timezone](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/get-current-time-in-specific-timezone/get-current-time-in-specific-timezone.mjs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `timezone` | body | `string` | yes | The IANA timezone name, e.g. `America/Los_Angeles`. [See the full list here](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones). |
