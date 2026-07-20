# OneMap SG: Get All Planning Areas

Retrieves all planning areas from OneMap SG.

```
GET https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-all-planning-areas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneMap SG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-all-planning-areas?connectionId=$CONNECTION_ID&year=2019" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2019"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-all-planning-areas?${params}`, {
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
| `year` | number | yes | The year to retrieve planning area polygons for. Example: `2019`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "SearchResults": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `SearchResults` | array<object> |  |

## Native endpoint

Through the native OneMap SG API, this operation is `GET /api/public/popapi/getAllPlanningarea` (base URL `https://www.onemap.gov.sg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-planning-areas.md) for the provider-specific parameters and requirements.

