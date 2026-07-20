# Hebcal: Get Hebrew Dates for Gregorian Range

Retrieves Hebrew dates for a Gregorian date range in Hebcal.

```
GET https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-hebrew-dates-for-gregorian-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hebcal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-hebrew-dates-for-gregorian-range?connectionId=$CONNECTION_ID&start=string&end=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "string",
  "end": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-hebrew-dates-for-gregorian-range?${params}`, {
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
| `start` | string | yes | Gregorian start date in YYYY-MM-DD format. |
| `end` | string | yes | Gregorian end date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end": "2026-05-07T12:00:00.000Z",
      "hdates": [
        [
          {}
        ]
      ],
      "start": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end` | date |  |
| `hdates[]` | array<object> |  |
| `hdates[].events[]` | array<string> |  |
| `hdates[].hd` | number |  |
| `hdates[].hebrew` | string |  |
| `hdates[].heDateParts.d` | string |  |
| `hdates[].heDateParts.m` | string |  |
| `hdates[].heDateParts.y` | string |  |
| `hdates[].hm` | string |  |
| `hdates[].hy` | number |  |
| `start` | date |  |

## Native endpoint

Through the native Hebcal API, this operation is `GET /converter` (base URL `https://www.hebcal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hebrew-dates-for-gregorian-range.md) for the provider-specific parameters and requirements.

