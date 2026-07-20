# Upload File From URL with Fibery

Creates a new file in Fibery from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/from-url`
- **Base URL:** `https://{account}.fibery.io/api`
- **Official documentation:** [Upload File From URL](https://the.fibery.io/@public/User_Guide/Guide/File-API-265)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Source file URL to upload into Fibery. |
| `name` | body | `string` | no | Optional filename to use inside Fibery. |
| `method` | body | `string` | no | HTTP method Fibery should use when downloading the source URL. |
