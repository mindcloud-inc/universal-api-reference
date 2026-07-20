# Get Code List Description with Finnish BIS

Retrieves code list details from Finnish BIS.

## Endpoint

- **Method:** `GET`
- **Path:** `/description`
- **Base URL:** `https://avoindata.prh.fi/opendata-ytj-api/v3`
- **Official documentation:** [Get Code List Description](https://avoindata.prh.fi/opendata-ytj-api/v3/schema?lang=en)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | query | `list<string>` | yes | PRH code list identifier to retrieve. Accepted values: `KIELI`, `KONK`, `REK`, `REK_KDI`, `SANE`, `SELTILA`, `SELTILA,SANE,KONK`, `STATUS3`, `TLAHDE`, `TLAJI`, `TOIMI`, `TOIMI2`, `TOIMI3`, `TOIMI4`, `VIRANOM`, `YRMU`. |
| `lang` | query | `list<string>` | yes | Language code for the code list description. Accepted values: `en`, `fi`, `sv`. |
