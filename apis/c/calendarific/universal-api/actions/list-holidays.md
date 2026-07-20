# Calendarific: List Holidays

Retrieves holidays from Calendarific by country and year.

```
GET https://connect.mindcloud.co/v1/universal/calendarific/latest/actions/list-holidays
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calendarific `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendarific/latest/actions/list-holidays?connectionId=$CONNECTION_ID&country=string&year=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "string",
  "year": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendarific/latest/actions/list-holidays?${params}`, {
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
| `country` | string | yes | ISO 3166 country code, such as US. |
| `year` | number | yes | Year to return holidays for. Calendarific supports historical and future years through 2049. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `month` | number | no | Optional month number from 1 to 12. |
| `day` | number | no | Optional day of month from 1 to 31. |
| `location` | string | no | Optional ISO 3166-2 state or region code, such as us-ny. |
| `type` | list<string> | no | Optional holiday type. Calendarific supports national, local, religious, and observance; multiple values can be comma-separated. One of: `0`, `1`, `2`, `3`. Accepts multiple values in one string, delimited by `,`. |
| `language` | string | no | Premium optional ISO 639 language code, such as fr. |
| `uuid` | boolean | no | Premium optional flag to return a UUID for every holiday. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canonicalUrl": "https://example.com",
      "country": {},
      "date": {},
      "description": "string",
      "locations": "string",
      "name": "Ava Chen",
      "primaryType": "string",
      "type": [
        "string"
      ],
      "urlid": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canonicalUrl` | string | Canonical Calendarific holiday URL. |
| `country` | object | Country identifier and display name. |
| `date` | object | Holiday date details. |
| `description` | string | Holiday description. |
| `locations` | string | Locations where the holiday applies. |
| `name` | string | Holiday name. |
| `primaryType` | string | Primary holiday classification. |
| `type` | array<string> | Holiday classification values. |
| `urlid` | string | Calendarific holiday URL identifier. |

## Native endpoint

Through the native Calendarific API, this operation is `GET /holidays` (base URL `https://calendarific.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-holidays.md) for the provider-specific parameters and requirements.

