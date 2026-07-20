# List Public Holidays with Festivo

Retrieves public holidays for a country and year from Festivo.

## Endpoint

- **Method:** `GET`
- **Path:** `/public-holidays/list`
- **Base URL:** `https://api.getfestivo.com/v3`
- **Official documentation:** [List Public Holidays](https://docs.getfestivo.com/docs/products/public-holidays-api/list-holidays/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | yes | ISO 3166-1 alpha-2 country code, for example US. |
| `year` | query | `number` | yes | Four-digit year to retrieve holidays for. |
| `month` | query | `number` | no | Optional month number from 1 to 12. |
| `day` | query | `number` | no | Optional day of month from 1 to 31. |
| `public` | query | `boolean` | no | Return only public holidays when true. |
| `before` | query | `boolean` | no | Premium filter: return only holidays before the specified date when true. |
| `after` | query | `boolean` | no | Premium filter: return only holidays after the specified date when true. |
| `format` | query | `list` | no | Response format. JSON is recommended. Accepted values: `0`, `1`. |
| `timezone` | query | `string` | no | Premium filter: TZ database timezone such as Europe/London. |
| `language` | query | `string` | no | Premium filter: ISO 639-1 language code such as en. |
| `regions` | query | `string` | no | Premium filter: comma-separated ISO 3166-2 subdivision or city region codes. Send multiple values as a string separated by `,`. |
