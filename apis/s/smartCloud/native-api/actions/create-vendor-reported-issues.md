# Report vendor issue with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/reported-issues`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Report vendor issue](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Issue type |
| `message` | body | `string` | yes | Message describing issue |
