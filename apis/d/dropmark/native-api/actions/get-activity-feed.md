# Get Activity Feed with Dropmark

## Endpoint

- **Method:** `GET`
- **Path:** `/activity.{{args.format}}`
- **Base URL:** `https://{subdomain}`
- **Official documentation:** [Get Activity Feed](https://support.dropmark.com/article/96-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | path | `string` | yes | Raw activity feed representation. Accepted values: `0`, `1`. |
