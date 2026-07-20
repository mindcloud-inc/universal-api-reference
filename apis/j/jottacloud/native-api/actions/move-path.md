# Move Path with Jottacloud

## Endpoint

- **Method:** `POST`
- **Path:** `/files/v2/move`
- **Base URL:** `https://api.jotta.cloud`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_path` | body | `string` | yes | Source logical path to move. |
| `to_path` | body | `string` | yes | Destination logical path for the moved item. |
