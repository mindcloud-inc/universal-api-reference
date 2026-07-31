# Generate Random Users with Random User

## Endpoint

- **Method:** `GET`
- **Path:** `/api/`
- **Base URL:** `https://randomuser.me`
- **Official documentation:** [Generate Random Users](https://randomuser.me/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `results` | query | `number` | no | Number of users to generate (1 to 5000). |
| `nat` | query | `list` | no | Optional nationalities to include. Accepted values: `0`, `1`, `10`, `11`, `12`, `13`, `14`, `15`, `16`, `17`, `18`, `19`, `2`, `20`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. Send multiple values as a string separated by `,`. |
| `gender` | query | `list` | no | Optional generated user gender. Accepted values: `0`, `1`. |
| `seed` | query | `string` | no | Optional deterministic seed for reproducible results. |
| `password` | query | `string` | no | Password grammar: charsets,MIN_LENGTH-MAX_LENGTH or charsets,MAX_LENGTH. |
| `inc` | query | `list` | no | Optional comma-delimited fields to include. Accepted values: `0`, `1`, `10`, `11`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. Send multiple values as a string separated by `,`. |
| `exc` | query | `list` | no | Optional comma-delimited fields to exclude. Accepted values: `0`, `1`, `10`, `11`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. Send multiple values as a string separated by `,`. |
