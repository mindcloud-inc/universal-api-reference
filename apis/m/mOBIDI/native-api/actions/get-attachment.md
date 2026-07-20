# Get Attachment with MOBIDI

Retrieves an attachment from a MOBIDI record.

## Endpoint

- **Method:** `POST`
- **Path:** `/MobidiQueryManagerHandler`
- **Base URL:** `https://servis2.dece.com.tr`
- **Official documentation:** [Get Attachment](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `recordId` | body | `string` | yes |
| `attachmentId` | body | `string` | yes |
| `download` | body | `boolean` | no |
