# Check Coverage with OTO

Checks delivery coverage in the OTO API.

## Endpoint

- **Method:** `POST`
- **Path:** `/checkCoverage`
- **Base URL:** `https://api.tryoto.com/rest/v2`
- **Official documentation:** [Check Coverage](https://help.tryoto.com/en/support/solutions/articles/150000213813-carrier-integrations-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | body | `string` | yes | Delivery latitude to check. |
| `lon` | body | `string` | yes | Delivery longitude to check. |
| `city` | body | `string` | yes | City name used in the coverage lookup. |
