# Create Signal with Das Keyboard 5Q

Creates a signal in Das Keyboard 5Q.

## Endpoint

- **Method:** `POST`
- **Path:** `/signals`
- **Base URL:** `https://q2.daskeyboard.com/api/1.0`
- **Official documentation:** [Create Signal](https://www.daskeyboard.io/api-ressources/signal/create-signal/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the signal. |
| `message` | body | `string` | no | Message displayed by the signal. |
| `zoneId` | body | `string` | yes | Keyboard zone targeted by the signal, such as KEY_Q, 74, or 2,2. |
| `color` | body | `string` | yes | Signal color as a hex value beginning with # and followed by 3 or 6 hexadecimal digits. |
| `effect` | body | `string` | no | Visual effect for the signal. |
| `pid` | body | `string` | yes | PID of the target Das Keyboard device, such as DK5QPID. |
| `isArchived` | body | `boolean` | no | Whether the signal is archived. Das Keyboard notes this is ignored on localhost. |
| `isRead` | body | `boolean` | no | Whether the signal is marked as read. Das Keyboard notes this is ignored on localhost. |
| `clientName` | body | `string` | no | Name of the client creating the signal, such as Zapier or Local Node Script. |
