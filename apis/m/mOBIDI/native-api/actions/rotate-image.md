# Rotate Image with MOBIDI

Rotates an image attachment in MOBIDI.

## Endpoint

- **Method:** `POST`
- **Path:** `/MobidiQueryManagerHandler`
- **Base URL:** `https://servis2.dece.com.tr`
- **Official documentation:** [Rotate Image](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `recordId` | body | `string` | yes |
| `attachmentId` | body | `string` | yes |
| `direction` | body | `number` | yes |
