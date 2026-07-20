# Manually trigger segment re-evaluation with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/contacts/groups/{id}/re-evaluate`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Manually trigger segment re-evaluation](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Segment ID to re-evaluate |
