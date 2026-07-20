# Create Enlarge Task with Bigjpg

Creates an image enlargement task in Bigjpg.

## Endpoint

- **Method:** `POST`
- **Path:** `/task/`
- **Base URL:** `https://bigjpg.com/api`
- **Official documentation:** [Create Enlarge Task](https://bigjpg.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Public URL of the image to enlarge. |
| `style` | body | `list` | yes | Bigjpg image style: art for illustrations or photo for photographs. Accepted values: `art`, `photo`. |
| `noise` | body | `list` | yes | Noise reduction level documented by Bigjpg. Accepted values: `-1`, `0`, `1`, `2`, `3`. |
| `x2` | body | `list` | yes | Upscale factor selector documented by Bigjpg. Accepted values: `1`, `2`, `3`, `4`. |
| `file_name` | body | `string` | no | Optional file name from the Bigjpg Python example. |
