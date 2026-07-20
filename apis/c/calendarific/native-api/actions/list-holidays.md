# List Holidays with Calendarific

Retrieves holidays from Calendarific by country and year.

## Endpoint

- **Method:** `GET`
- **Path:** `/holidays`
- **Base URL:** `https://calendarific.com/api/v2`
- **Official documentation:** [List Holidays](https://calendarific.com/api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | yes | ISO 3166 country code, such as US. |
| `year` | query | `number` | yes | Year to return holidays for. Calendarific supports historical and future years through 2049. |
| `month` | query | `number` | no | Optional month number from 1 to 12. |
| `day` | query | `number` | no | Optional day of month from 1 to 31. |
| `location` | query | `string` | no | Optional ISO 3166-2 state or region code, such as us-ny. |
| `type` | query | `list<string>` | no | Optional holiday type. Calendarific supports national, local, religious, and observance; multiple values can be comma-separated. Accepted values: `0`, `1`, `2`, `3`. Send multiple values as a string separated by `,`. |
| `language` | query | `string` | no | Premium optional ISO 639 language code, such as fr. |
| `uuid` | query | `boolean` | no | Premium optional flag to return a UUID for every holiday. |
