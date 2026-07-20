# Find Email with Gamalogic

## Endpoint

- **Method:** `GET`
- **Path:** `/email-discovery`
- **Base URL:** `https://gamalogic.com`
- **Official documentation:** [Find Email](https://docs.gamalogic.com/find-email/single-email-finder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstname` | query | `string` | yes | First name of the lead. |
| `lastname` | query | `string` | yes | Last name of the lead. |
| `domain` | query | `string` | yes | Company domain or URL to search. |
| `speed_rank` | query | `number` | no | Optional speed and accuracy setting. Defaults to 0; higher values are slower and more accurate. |
