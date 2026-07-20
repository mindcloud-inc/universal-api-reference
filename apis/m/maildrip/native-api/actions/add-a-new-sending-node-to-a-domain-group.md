# Add a new sending node to a domain group with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/mumara/sending-nodes`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Add a new sending node to a domain group](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | MongoDB User ID |
| `domainGroupId` | body | `string` | yes | Domain Group UUID |
| `nodeType` | body | `string` | yes | — |
| `name` | body | `string` | yes | Name for the sending node |
| `domainId` | body | `string` | no | Optional domain ID from Mumara |
| `replyTo` | body | `string` | no | Reply-to email address |
| `emailFrom` | body | `string` | no | From email display name/address |
| `status` | body | `number` | no | Node status (0=inactive, 1=active) |
| `host` | body | `string` | yes | SMTP host |
| `port` | body | `number` | yes | SMTP port |
| `username` | body | `string` | yes | SMTP username |
| `password` | body | `string` | yes | SMTP password |
| `encryptionMethod` | body | `string` | no | Encryption method |
| `mailEncoding` | body | `string` | no | Mail encoding |
