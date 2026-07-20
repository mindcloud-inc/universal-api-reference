# Melo: List Cities

Retrieves cities from Melo matching the provided criteria.

```
GET https://connect.mindcloud.co/v1/universal/melo/latest/actions/list-cities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Melo `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/melo/latest/actions/list-cities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/melo/latest/actions/list-cities?${params}`, {
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
| `page` | number | no | Collection page number. Default: `1`. |
| `name` | string | no | Filter by city name. |
| `zipcode` | string | no | Filter by zipcode. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "article": "string",
      "cityParent": {},
      "department": "string",
      "insee": "string",
      "latitude": 1,
      "libelle": "string",
      "longitude": 1,
      "name": "Ava Chen",
      "originalName": "Ava Chen",
      "zipcode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `article` | string |  |
| `cityParent` | object |  |
| `department` | string |  |
| `insee` | string |  |
| `latitude` | number |  |
| `libelle` | string |  |
| `longitude` | number |  |
| `name` | string |  |
| `originalName` | string |  |
| `zipcode` | string |  |

## Native endpoint

Through the native Melo API, this operation is `GET /cities` (base URL `https://preprod-api.notif.immo`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cities.md) for the provider-specific parameters and requirements.

