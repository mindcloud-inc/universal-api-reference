# Get cluster with Starburst Galaxy

## Endpoint

- **Method:** `GET`
- **Path:** `/public/api/v1/cluster/{clusterId}`
- **Base URL:** `https://mindcloud.galaxy.starburst.io`
- **Official documentation:** [Get cluster](https://galaxy.starburst.io/public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clusterId` | path | `string` | yes | Starburst Galaxy cluster ID. Docs also support URL-encoded lookup expressions such as name=value. |
| `extended` | query | `boolean` | no | Whether to include extended cluster details when supported by Starburst Galaxy. |
