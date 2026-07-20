# Create PubSub Token with SignalWire

Creates a new PubSub token in SignalWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/pubsub/tokens`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Create PubSub Token](https://signalwire.com/docs/apis/rest/pubsub/create-token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ttl` | body | `number` | yes | The maximum time, in minutes, for which the access token will be valid. Between 1 and 43,200 (30 days). |
| `channels` | body | `object` | yes | Each channel with `write` and `read` objects with boolean as values. Max of 500 channels inside main `channels`.  Either `read`, `write`, or both are required inside each channel and default to false.  Each channel name can be up to 250 characters. Must be valid JSON. |
| `member_id` | body | `string` | no | The unique identifier of the member. Up to 250 characters. If not specified, a random UUID will be generated. |
| `state` | body | `object` | no | An arbitrary JSON object available to store stateful application information in. Must be valid JSON and have a maximum size of 2,000 characters. |
