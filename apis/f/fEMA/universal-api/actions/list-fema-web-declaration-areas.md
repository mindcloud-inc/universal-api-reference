# FEMA: List FEMA Web Declaration Areas

Retrieves FEMA web declaration areas.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-fema-web-declaration-areas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-fema-web-declaration-areas?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-fema-web-declaration-areas?${params}`, {
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
      "closeoutDate": "2026-05-07T12:00:00.000Z",
      "designatedDate": "2026-05-07T12:00:00.000Z",
      "disasterNumber": 1,
      "entryDate": "2026-05-07T12:00:00.000Z",
      "hash": "string",
      "id": "string",
      "lastRefresh": "2026-05-07T12:00:00.000Z",
      "placeCode": "string",
      "placeName": "Ava Chen",
      "programTypeCode": "string",
      "programTypeDescription": "string",
      "stateCode": "string",
      "stateName": "Ava Chen",
      "updateDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `closeoutDate` | date |  |
| `designatedDate` | date |  |
| `disasterNumber` | number |  |
| `entryDate` | date |  |
| `hash` | string |  |
| `id` | string |  |
| `lastRefresh` | date |  |
| `placeCode` | string |  |
| `placeName` | string |  |
| `programTypeCode` | string |  |
| `programTypeDescription` | string |  |
| `stateCode` | string |  |
| `stateName` | string |  |
| `updateDate` | date |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/FemaWebDeclarationAreas` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-fema-web-declaration-areas.md) for the provider-specific parameters and requirements.

