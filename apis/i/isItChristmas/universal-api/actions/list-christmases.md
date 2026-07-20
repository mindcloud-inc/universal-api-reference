# Is It Christmas?: List Christmases



```
GET https://connect.mindcloud.co/v1/universal/isItChristmas/latest/actions/list-christmases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Is It Christmas? `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/isItChristmas/latest/actions/list-christmases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/isItChristmas/latest/actions/list-christmases?${params}`, {
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
| `country` | string | no | ISO 3166-1 alpha-2 country code used for localized yes/no text. Example: `US`. |
| `timezone` | string | no | IANA timezone name used to calculate Christmas in that zone. Example: `UTC`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "christmas": true,
      "christmas_day": "2026-05-07T12:00:00.000Z",
      "christmas_time": 1,
      "country": "string",
      "country_names": [
        "Ava Chen"
      ],
      "id": "string",
      "timezone": "string",
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string | Localized yes/no string for the requested country. |
| `christmas` | boolean | Whether the returned row represents Christmas Day. |
| `christmas_day` | date | ISO timestamp for Christmas Day in the requested timezone. |
| `christmas_time` | number | Unix timestamp for Christmas Day. |
| `country` | string | ISO 3166-1 alpha-2 country code. |
| `country_names` | array<string> | Localized country names returned by the provider. |
| `id` | string | Stable Christmas occurrence identifier. |
| `timezone` | string | IANA timezone used for the calculation. |
| `year` | number | Calendar year for the Christmas occurrence. |

## Native endpoint

Through the native Is It Christmas? API, this operation is `GET /api` (base URL `https://isitchristmas.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-christmases.md) for the provider-specific parameters and requirements.

