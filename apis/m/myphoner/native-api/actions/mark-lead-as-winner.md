# Mark Lead as Winner with Myphoner

Marks a lead as a winner in Myphoner.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/:leadId/winner`
- **Base URL:** `https://{subdomain}.myphoner.com/api/v2`
- **Official documentation:** [Mark Lead as Winner](https://www.myphoner.com/docs/api/#leads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `call_back_in` | body | `number` | no | Minutes until the scheduled call back. |
| `category` | body | `string` | no | Existing Myphoner category to apply exactly as named. |
| `comment` | body | `string` | no | Comment text to attach to the lead event. |
| `leadId` | path | `number` | yes | The Myphoner lead ID. |
| `scheduled_for` | body | `date` | no | UTC datetime for the scheduled call back. Takes precedence over Call Back In when present. |
