# Get System Engine URL with Firebolt

Retrieves a system engine URL from Firebolt.

## Endpoint

- **Method:** `GET`
- **Path:** `/web/v3/account/:accountName/engineUrl`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Get System Engine URL](https://docs.firebolt.io/guides/developing-with-firebolt/using-the-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountName` | path | `string` | yes | The Firebolt account name used in the engineUrl bootstrap path. |
