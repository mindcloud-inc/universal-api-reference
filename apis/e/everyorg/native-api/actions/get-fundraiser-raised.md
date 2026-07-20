# Get Fundraiser Raised with Every.org

Retrieves raised totals for a fundraiser from Every.org.

## Endpoint

- **Method:** `GET`
- **Path:** `/nonprofit/:nonprofitIdentifier/fundraiser/:fundraiserIdentifier/raised`
- **Base URL:** `https://partners.every.org/v0.2`
- **Official documentation:** [Get Fundraiser Raised](https://docs.every.org/docs/endpoints/fundraisers#get-v02nonprofitnonprofitidentifierfundraiserfundraiseridentifierraised)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nonprofitIdentifier` | path | `string` | yes | A nonprofit slug, EIN, nonprofit ID, or special-fundraiser for multi-nonprofit fundraisers. |
| `fundraiserIdentifier` | path | `string` | yes | Fundraiser slug or identifier. |
