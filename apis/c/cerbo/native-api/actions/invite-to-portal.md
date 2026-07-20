# Invite To Portal with Cerbo

Sends a Cerbo patient portal invitation email.

## Endpoint

- **Method:** `POST`
- **Path:** `/patients/:pt_id/portal/invite`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Invite To Portal](https://docs.cer.bo/#tag/Patient-Portal/operation/inviteToPortal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pt_id` | path | `number` | no | ID of patient |
