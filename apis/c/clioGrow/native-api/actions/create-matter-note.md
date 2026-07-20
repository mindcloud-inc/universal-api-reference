# Create Matter Note with Clio Grow

## Endpoint

- **Method:** `POST`
- **Path:** `/matters/{matter_id}/notes`
- **Base URL:** `https://api.clio.com/grow`
- **Official documentation:** [Create Matter Note](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Matters/operation/MatterNote%23create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `matter_id` | path | `string` | yes | The unique identifier for the matter. |
| `data.subject` | body | `string` | yes | Subject line of the note. Maximum length: 255. |
| `data.body` | body | `string` | yes | Body content of the note. Maximum length: 65535. |
