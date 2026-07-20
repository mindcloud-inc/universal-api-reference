# Enroll in Sequence with Hy.page

## Endpoint

- **Method:** `POST`
- **Path:** `/hyax-api/v1/sequences/enroll`
- **Base URL:** `https://platform.hyax.com`
- **Official documentation:** [Enroll in Sequence](https://platform.hyax.com/api-docs/sequence-enroll)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Existing person's email address. |
| `sequenceId` | body | `string` | yes | Email sequence ID. |
