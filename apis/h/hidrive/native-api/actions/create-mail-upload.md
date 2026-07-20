# Create Mail Upload with HiDrive

Creates a new mail upload in HiDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/mailupload`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Create Mail Upload](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/mailupload_POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | no | Directory path for the mail upload. |
| `pid` | body | `string` | no | Directory public ID for the mail upload. |
| `rcpt_secret` | body | `string` | no | Secret component for the mail upload address. |
| `rcpt_string` | body | `string` | no | Local part of the generated mail upload address. |
| `unique` | body | `string` | no | Unique identifier returned by Get Unique Identifier. |
| `unique_mac` | body | `string` | no | MAC returned with the unique identifier. |
| `ttl` | body | `number` | no | Mail upload expiry in seconds. |
| `overwrite` | body | `boolean` | no | Allow uploaded files to overwrite existing files. |
| `reportok` | body | `boolean` | no | Send success notification report. |
