# Create Website with Umami

## Endpoint

- **Method:** `POST`
- **Path:** `/websites`
- **Base URL:** `https://api.umami.is/v1`
- **Official documentation:** [Create Website](https://docs.umami.is/docs/api/websites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The website name in Umami. |
| `domain` | body | `string` | yes | The full tracked domain. |
| `shareId` | body | `string` | no | A share URL identifier. Set null to unshare. |
| `teamId` | body | `string` | no | The team ID the website will be created under. |
