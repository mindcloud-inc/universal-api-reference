# Api to restore page history with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/history/restore`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Api to restore page history](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `pageID` | body | `string` | yes | — |
| `versionID` | body | `string` | yes | — |
