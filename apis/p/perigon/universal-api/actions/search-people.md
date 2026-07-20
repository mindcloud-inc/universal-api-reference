# Perigon: Search People

Finds people in Perigon by name or Wikidata details.

```
GET https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perigon `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-people?${params}`, {
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
| `name` | string | no | Example: `Elon Musk`. |
| `wikidataId` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `Q317521`. |
| `occupationId` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `Q82955`. |
| `occupationLabel` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `politician`. |
| `page` | number | no | Example: `0`. |
| `size` | number | no | Example: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "numResults": 1,
      "results": [
        {}
      ],
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `numResults` | number |  |
| `results` | array<object> |  |
| `status` | number |  |

## Native endpoint

Through the native Perigon API, this operation is `GET /v1/people/all` (base URL `https://api.perigon.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-people.md) for the provider-specific parameters and requirements.

