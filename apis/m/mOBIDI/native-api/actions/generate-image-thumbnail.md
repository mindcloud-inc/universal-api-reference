# Generate Image Thumbnail with MOBIDI

Generates an image thumbnail for a MOBIDI attachment.

## Endpoint

- **Method:** `POST`
- **Path:** `/MobidiQueryManagerHandler`
- **Base URL:** `https://servis2.dece.com.tr`
- **Official documentation:** [Generate Image Thumbnail](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recordId` | body | `string` | yes | MOBIDI record identifier. |
| `attachmentId` | body | `string` | yes | Attachment identifier. |
| `maxSize` | body | `number` | yes | Maximum thumbnail size in pixels. |
