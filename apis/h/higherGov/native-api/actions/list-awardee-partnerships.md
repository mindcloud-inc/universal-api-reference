# List Awardee Partnerships with HigherGov

Retrieves awardee partnerships from HigherGov.

## Endpoint

- **Method:** `GET`
- **Path:** `/api-external/awardee-partnership/`
- **Base URL:** `https://www.highergov.com`
- **Official documentation:** [List Awardee Partnerships](https://www.highergov.com/api-external/docs/#/api-external/api_external_awardee_partnership_list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `awardee_key_prime` | query | `string` | no | HigherGov Awardee Key of the prime recipient |
| `awardee_key_prime_parent` | query | `string` | no | HigherGov Awardee Key of the prime recipient parent |
| `awardee_key_sub` | query | `string` | no | HigherGov Awardee Key of the subawardee |
| `awardee_key_sub_parent` | query | `string` | no | HigherGov Awardee Key of the subawardee parent |
