# Fiddle: List Measurement Units

Retrieves measurement unit records from Fiddle.

```
GET https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-measurement-units
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiddle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-measurement-units?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-measurement-units?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "measurementUnits": [
        {
          "abbreviation": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "name": "Ava Chen",
          "unitType": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `measurementUnits` | array<object> |  |
| `measurementUnits[].abbreviation` | string |  |
| `measurementUnits[].createdAt` | date |  |
| `measurementUnits[].id` | string |  |
| `measurementUnits[].name` | string |  |
| `measurementUnits[].unitType` | string |  |
| `measurementUnits[].updatedAt` | date |  |

## Native endpoint

Through the native Fiddle API, this operation is `GET /measurement-units` (base URL `https://fiddle.io/rest/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-measurement-units.md) for the provider-specific parameters and requirements.

