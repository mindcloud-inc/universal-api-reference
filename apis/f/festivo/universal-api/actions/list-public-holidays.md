# Festivo: List Public Holidays

Retrieves public holidays for a country and year from Festivo.

```
GET https://connect.mindcloud.co/v1/universal/festivo/latest/actions/list-public-holidays
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Festivo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/festivo/latest/actions/list-public-holidays?connectionId=$CONNECTION_ID&country=US&year=2026" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "US",
  "year": "2026"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/festivo/latest/actions/list-public-holidays?${params}`, {
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
| `country` | string | yes | ISO 3166-1 alpha-2 country code, for example US. Example: `US`. |
| `year` | number | yes | Four-digit year to retrieve holidays for. Example: `2026`. |
| `month` | number | no | Optional month number from 1 to 12. Example: `1`. |
| `day` | number | no | Optional day of month from 1 to 31. Example: `1`. |
| `public` | boolean | no | Return only public holidays when true. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `before` | boolean | no | Premium filter: return only holidays before the specified date when true. |
| `after` | boolean | no | Premium filter: return only holidays after the specified date when true. |
| `format` | list | no | Response format. JSON is recommended. One of: `0`, `1`. Default: `json`. |
| `timezone` | string | no | Premium filter: TZ database timezone such as Europe/London. Example: `Europe/London`. |
| `language` | string | no | Premium filter: ISO 639-1 language code such as en. Example: `en`. |
| `regions` | string | no | Premium filter: comma-separated ISO 3166-2 subdivision or city region codes. Accepts multiple values in one string, delimited by `,`. Example: `GB-ENG`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "dataVersion": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "deprecated": true,
      "end": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "name_local": "Ava Chen",
      "observed": "2026-05-07T12:00:00.000Z",
      "public": true,
      "regions": [
        {}
      ],
      "start": "2026-05-07T12:00:00.000Z",
      "subdivisions": [
        "string"
      ],
      "substitute": true,
      "type": "string",
      "weekday": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string | ISO 3166-1 alpha-2 country code. |
| `dataVersion` | string | Festivo data version. |
| `date` | date | Date the holiday occurs. |
| `deprecated` | boolean | Whether the holiday record is deprecated. |
| `end` | date | End date/time for the holiday. |
| `id` | string | Festivo holiday identifier. |
| `name` | string | Holiday or observance name. |
| `name_local` | string | Local-language holiday name when available. |
| `observed` | date | Date the holiday is observed. |
| `public` | boolean | Whether the holiday is a public holiday. |
| `regions` | array<object> | Region metadata for city or subdivision-specific holidays. |
| `start` | date | Start date/time for the holiday. |
| `subdivisions` | array<string> | ISO 3166-2 subdivision codes for the holiday. |
| `substitute` | boolean | Whether this is a substitute holiday. |
| `type` | string | Holiday type such as public, regional, observance, or bank. |
| `weekday` | object | Weekday metadata for date and observed date. |

## Native endpoint

Through the native Festivo API, this operation is `GET /public-holidays/list` (base URL `https://api.getfestivo.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-public-holidays.md) for the provider-specific parameters and requirements.

