# Assign Label to Contact Profile with SuperSend

Assigns a profile label to a SuperSend contact.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/{id}/profile-labels`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Assign Label to Contact Profile](https://docs.supersend.io/docs/contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Resource ID (UUID) |
| `label_id` | body | `string` | yes | — |
