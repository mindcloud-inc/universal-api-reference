# Create Tale From Text with TAYL

## Endpoint

- **Method:** `POST`
- **Path:** `/submit`
- **Base URL:** `https://x.tayl.app`
- **Official documentation:** [Create Tale From Text](https://my.tayl.app/create/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Title for the text-based tale. |
| `markup` | body | `string` | yes | HTML markup or rich text content to convert into a tale. |
