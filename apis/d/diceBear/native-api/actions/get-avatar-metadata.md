# Get Avatar Metadata with DiceBear

## Endpoint

- **Method:** `GET`
- **Path:** `/:styleName/json`
- **Base URL:** `https://api.dicebear.com/10.x`
- **Official documentation:** [Get Avatar Metadata](https://www.dicebear.com/how-to-use/http-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleName` | path | `string` | yes | A current DiceBear 10.x style name in lowercase, using hyphens for multiple words (for example, adventurer-neutral). |
| `seed` | query | `string` | no | Seed used to generate a deterministic avatar. |
