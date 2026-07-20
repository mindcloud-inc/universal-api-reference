# Create Group with Sempico Solutions SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/group-create`
- **Base URL:** `https://restapi.sempico.solutions/v1`
- **Official documentation:** [Create Group](https://pypi.org/pypi/gatum-rest-py/json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name_group` | body | `string` | yes | Name for the new group. |
| `time_birth` | body | `string` | no | Optional time for birthday greeting messages. |
| `originator_birth` | body | `string` | no | Optional sender ID for birthday greeting messages. |
| `text_birth` | body | `string` | no | Optional birthday greeting text. Sempico supports replacing #first_name# with the contact name. |
| `on_birth` | body | `boolean` | no | Whether birthday greetings should be sent for this group. |
