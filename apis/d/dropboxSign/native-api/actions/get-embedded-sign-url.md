# Get Embedded Sign URL with Dropbox Sign

Retrieves an embedded signing URL from Dropbox Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/embedded/sign_url/:signature_id`
- **Base URL:** `https://api.hellosign.com/v3`
- **Official documentation:** [Get Embedded Sign URL](https://developers.hellosign.com/api/reference/operation/embeddedSignUrl/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signature_id` | path | `string` | yes | The id of the signature to get a sign URL for. |
