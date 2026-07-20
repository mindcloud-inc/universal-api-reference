# Create Issue with Cursion

## Endpoint

- **Method:** `POST`
- **Path:** `/issue`
- **Base URL:** `https://api.cursion.dev/v1/ops`
- **Official documentation:** [Create Issue](https://docs.cursion.dev/api/issue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affected` | body | `object` | yes | The affected resource object with id, str, and type. |
| `details` | body | `string` | yes | The issue details in Markdown. |
| `title` | body | `string` | yes | The issue title. |
| `trigger` | body | `object` | yes | The trigger object with id and type. |
