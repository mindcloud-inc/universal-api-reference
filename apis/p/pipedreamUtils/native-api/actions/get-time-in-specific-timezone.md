# Helper Functions - Get Time in Timezone with Pipedream Utils

Converts an ISO timestamp to a timezone in Pipedream Utils.

## Endpoint

- **Method:** `GET`
- **Base URL:** `https://pipedream.com`
- **Official documentation:** [Helper Functions - Get Time in Timezone](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/get-time-in-specific-timezone/get-time-in-specific-timezone.mjs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `time` | body | `string` | yes | An [ISO 8601 string](https://en.wikipedia.org/wiki/ISO_8601) representing the time you'd like to convert to your target timezone. If this timestamp doesn't have a timezone component, it's assumed to be in UTC. |
| `timezone` | body | `string` | yes | The IANA timezone name, e.g. `America/Los_Angeles`. [See the full list here](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones). |
