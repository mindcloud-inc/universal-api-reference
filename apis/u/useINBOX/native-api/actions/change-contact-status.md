# Change Contact Status with UseINBOX

Updates a contact's status in UseINBOX.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/inbox/v1/contacts/:id/status`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Change Contact Status](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Contact ID from INBOX. |
| `status` | body | `number` | yes | INBOX contact status value. Docs list 2 hard bounce, 3 unsubscribe, and 4 spam reported. |
