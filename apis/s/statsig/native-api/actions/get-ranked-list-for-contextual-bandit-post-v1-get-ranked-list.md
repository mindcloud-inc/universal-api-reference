# Get Ranked List for Contextual Bandit with Statsig

Retrieves a ranked list from Statsig for contextual bandits.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/get_ranked_list`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Get Ranked List for Contextual Bandit](https://docs.statsig.com/api-reference/autotune/get-ranked-list-for-contextual-bandit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `configName` | body | `string` | yes | Name of the contextual bandit/autotune experiment. |
| `user` | body | `object` | yes | Statsig user object containing at least one identifier. |
| `statsigMetadata` | body | `object` | no | SDK metadata for diagnostics and exposure behavior. |
