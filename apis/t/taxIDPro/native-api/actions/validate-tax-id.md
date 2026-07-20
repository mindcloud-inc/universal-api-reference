# Validate Tax ID with Tax ID Pro

Retrieves a tax ID validation from Tax ID Pro.

## Endpoint

- **Method:** `GET`
- **Path:** `/validate`
- **Base URL:** `https://v3.api.taxid.pro`
- **Official documentation:** [Validate Tax ID](https://taxid.pro/docs/tax-id-validation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | yes | Two-letter country code as defined in the ISO standard. Use IRS country codes only when Is IRS is true. |
| `tin` | query | `string` | yes | Tax ID number. It may contain numbers, letters, dots, dashes, or slashes when those separators match the tax ID format being tested. |
| `type` | query | `string` | no | Optional tax ID type. Use individual, entity, or vat; omit to test all available types for the country. Accepted values: `0`, `1`, `2`. |
| `locale` | query | `string` | no | Optional language tag for the message property. Use auto for the language most appropriate for the country, or one of the documented locales. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. |
| `is_irs` | query | `boolean` | no | Set true when country uses IRS country codes instead of ISO country codes. |
