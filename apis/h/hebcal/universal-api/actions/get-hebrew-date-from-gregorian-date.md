# Hebcal: Get Hebrew Date from Gregorian Date

Retrieves a Hebrew date from a Gregorian date in Hebcal.

```
GET https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-hebrew-date-from-gregorian-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hebcal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-hebrew-date-from-gregorian-date?connectionId=$CONNECTION_ID&date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-hebrew-date-from-gregorian-date?${params}`, {
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
| `date` | string | yes | Gregorian date in YYYY-MM-DD format. |
| `strict` | string | no | Return an error for invalid dates when enabled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "afterSunset": true,
      "events": [
        [
          "string"
        ]
      ],
      "gd": 1,
      "gm": 1,
      "gy": 1,
      "hd": 1,
      "hebrew": "string",
      "heDateParts": {
        "d": "string",
        "m": "string",
        "y": "string"
      },
      "hm": "string",
      "hy": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `afterSunset` | boolean |  |
| `events[]` | array<string> |  |
| `gd` | number |  |
| `gm` | number |  |
| `gy` | number |  |
| `hd` | number |  |
| `hebrew` | string |  |
| `heDateParts.d` | string |  |
| `heDateParts.m` | string |  |
| `heDateParts.y` | string |  |
| `hm` | string |  |
| `hy` | number |  |

## Native endpoint

Through the native Hebcal API, this operation is `GET /converter` (base URL `https://www.hebcal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hebrew-date-from-gregorian-date.md) for the provider-specific parameters and requirements.

