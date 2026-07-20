# Delete Mail Upload with HiDrive

Deletes a mail upload from HiDrive.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/mailupload`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Delete Mail Upload](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/mailupload_DELETE)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | yes | Mail upload path to delete. |
| `pid` | body | `string` | no | Mail upload public ID to delete. |
