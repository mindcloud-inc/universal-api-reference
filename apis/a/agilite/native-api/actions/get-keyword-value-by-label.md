# Get Keyword Value By Label with Agilite

Retrieves a keyword value from Agilite by profile and label key.

## Endpoint

- **Method:** `GET`
- **Path:** `/keywords/getValueByLabel`
- **Base URL:** `https://api.agilite.io`
- **Official documentation:** [Get Keyword Value By Label](https://docs.agilite.io/reference/getvaluebylabel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile-key` | query | `string` | yes | Agilit-e keyword profile key. |
| `label-key` | query | `string` | yes | Keyword label key to resolve. |
