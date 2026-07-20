# Abstract Holidays: Get Holidays

Retrieves holidays from Abstract Holidays for a country and date.

```
GET https://connect.mindcloud.co/v1/universal/abstractHolidays/latest/actions/get-holidays
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Abstract Holidays `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abstractHolidays/latest/actions/get-holidays?connectionId=$CONNECTION_ID&country=US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abstractHolidays/latest/actions/get-holidays?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `country` | string | yes | Two-letter ISO 3166-1 alpha-2 country code, such as US or SG. Default: `US`. Example: `US`. |
| `year` | string | no | Four-digit year to retrieve holidays for. Required for Abstract free-plan connections and for month/day queries; paid plans may support defaulting for broader lookups. Default: `2026`. Example: `2026`. |
| `month` | string | no | Month to retrieve, formatted as 01-12. Required for Abstract free-plan individual-day lookups and whenever Day is provided. Default: `01`. Example: `01`. |
| `day` | string | no | Day of month to retrieve, formatted as 01-31. Use with Year and Month for the current verified free-plan lookup path. Default: `01`. Example: `01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "date": "string",
      "date_day": "string",
      "date_month": "string",
      "date_year": "string",
      "description": "string",
      "language": "string",
      "location": "string",
      "name": "Ava Chen",
      "name_local": "Ava Chen",
      "type": "string",
      "week_day": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string | Two-letter country code. |
| `date` | string | Holiday date as returned by Abstract, commonly MM/DD/YYYY. |
| `date_day` | string | Holiday day of month. |
| `date_month` | string | Holiday month. |
| `date_year` | string | Holiday year. |
| `description` | string | Holiday description when provided. |
| `language` | string | Language code or label for the localized holiday name when provided. |
| `location` | string | Country or local jurisdiction where the holiday applies. |
| `name` | string | Holiday name. |
| `name_local` | string | Holiday name in the local language when provided. |
| `type` | string | Holiday type, such as National. |
| `week_day` | string | Day of the week. |

## Native endpoint

Through the native Abstract Holidays API, this operation is `GET /v1/` (base URL `https://holidays.abstractapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-holidays.md) for the provider-specific parameters and requirements.

