# Post To Page Discussion with Papyrs

## Endpoint

- **Method:** `POST`
- **Path:** `/feed/post/:page_id/`
- **Base URL:** `https://{subdomain}.papyrs.com/api/v1`
- **Official documentation:** [Post To Page Discussion](https://papyrs.com/docs/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msg` | body | `string` | yes | The message to post to the page discussion. |
| `page_id` | path | `string` | yes | The Papyrs page ID. |
