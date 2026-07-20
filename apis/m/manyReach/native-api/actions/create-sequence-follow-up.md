# Create Sequence Follow-Up with ManyReach

Creates a follow-up for a sequence in ManyReach.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.manyreach.com/api/v2/sequences/:id/followups`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [Create Sequence Follow-Up](https://api.manyreach.com/api#v2/tag/sequence)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Sequence ID. |
| `waitMin` | body | `string` | yes | Wait duration amount before the follow-up. |
| `waitUnits` | body | `string` | yes | Units for the wait duration. |
