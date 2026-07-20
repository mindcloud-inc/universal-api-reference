# Get CreditSafe Rating with Lasso X

Retrieves a CreditSafe rating from Lasso X by CVR number.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/creditsafe/rating/:cvr`
- **Base URL:** `https://api.lassox.com`
- **Official documentation:** [Get CreditSafe Rating](https://docs.lassox.com/data-apis/creditsafe/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cvr` | path | `number` | yes | Danish CVR company number. |
