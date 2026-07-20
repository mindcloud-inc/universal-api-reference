# Invite Candidates with Testfuse

Invites candidates to a Testfuse assessment spec.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users/invite_multiple_candidates`
- **Base URL:** `https://gateway.testfuse.com`
- **Official documentation:** [Invite Candidates](https://api.testfuse.com)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes |
| `spec_id` | body | `string` | yes |
