# Upload Attachment with MOBIDI

Uploads an attachment to a MOBIDI record.

## Endpoint

- **Method:** `POST`
- **Path:** `/MobidiQueryManagerHandler`
- **Base URL:** `https://servis2.dece.com.tr`
- **Official documentation:** [Upload Attachment](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileName` | body | `string` | yes | Attachment file name. |
| `layer_id` | body | `string` | yes | Target layer identifier. |
| `record_id` | body | `string` | yes | Target record identifier. |
| `guid` | body | `string` | yes | Upload GUID token. |
