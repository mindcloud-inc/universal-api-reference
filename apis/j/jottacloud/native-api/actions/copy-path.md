# Copy Path with Jottacloud

## Endpoint

- **Method:** `POST`
- **Path:** `/files/v2/copy`
- **Base URL:** `https://api.jotta.cloud`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_path` | body | `string` | yes | Source logical path to copy. |
| `to_path` | body | `string` | yes | Destination logical path for the copied item. |
