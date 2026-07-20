# List Mentor Protege Relationships with HigherGov

Retrieves mentor-protege relationships from HigherGov.

## Endpoint

- **Method:** `GET`
- **Path:** `/api-external/awardee-mp/`
- **Base URL:** `https://www.highergov.com`
- **Official documentation:** [List Mentor Protege Relationships](https://www.highergov.com/api-external/docs/#/api-external/api_external_awardee_mp_list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `awardee_key_mentor` | query | `string` | no | HigherGov Awardee Key of the mentor |
| `awardee_key_mentor_parent` | query | `string` | no | HigherGov Awardee Key of the mentor parent |
| `awardee_key_protege` | query | `string` | no | HigherGov Awardee Key of the protege |
| `awardee_key_protege_parent` | query | `string` | no | HigherGov Awardee Key of the protege parent |
