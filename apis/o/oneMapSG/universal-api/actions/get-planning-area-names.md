# OneMap SG: Get Planning Area Names

Retrieves planning area names from OneMap SG.

```
GET https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-planning-area-names
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneMap SG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-planning-area-names?connectionId=$CONNECTION_ID&year=2019" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2019"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-planning-area-names?${params}`, {
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
| `year` | number | yes | The year to retrieve planning area names for. Example: `2019`. |

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

Through the native OneMap SG API, this operation is `GET /api/public/popapi/getPlanningareaNames` (base URL `https://www.onemap.gov.sg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-planning-area-names.md) for the provider-specific parameters and requirements.

