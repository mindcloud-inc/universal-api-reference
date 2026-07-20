# Get Topic By External ID with Discourse

Retrieves a Discourse topic by external ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/t/external_id/:external_id.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Get Topic By External ID](https://docs.discourse.org/#tag/Topics/operation/getTopicByExternalId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `external_id` | path | `string` | yes | External topic identifier configured in Discourse. |
