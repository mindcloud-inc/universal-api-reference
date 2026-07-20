# FEMA: List FEMA Web Disaster Declarations

Retrieves FEMA web disaster declarations.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-fema-web-disaster-declarations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-fema-web-disaster-declarations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-fema-web-disaster-declarations?${params}`, {
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
      "declarationDate": "2026-05-07T12:00:00.000Z",
      "declarationType": "string",
      "disasterName": "Ava Chen",
      "disasterNumber": 1,
      "disasterPageUrl": "https://example.com",
      "hash": "string",
      "hmProgramDeclared": true,
      "iaProgramDeclared": true,
      "id": "string",
      "ihProgramDeclared": true,
      "incidentBeginDate": "2026-05-07T12:00:00.000Z",
      "incidentEndDate": "2026-05-07T12:00:00.000Z",
      "incidentType": "string",
      "lastRefresh": "2026-05-07T12:00:00.000Z",
      "paProgramDeclared": true,
      "region": 1,
      "stateCode": "string",
      "stateName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `declarationDate` | date |  |
| `declarationType` | string |  |
| `disasterName` | string |  |
| `disasterNumber` | number |  |
| `disasterPageUrl` | string |  |
| `hash` | string |  |
| `hmProgramDeclared` | boolean |  |
| `iaProgramDeclared` | boolean |  |
| `id` | string |  |
| `ihProgramDeclared` | boolean |  |
| `incidentBeginDate` | date |  |
| `incidentEndDate` | date |  |
| `incidentType` | string |  |
| `lastRefresh` | date |  |
| `paProgramDeclared` | boolean |  |
| `region` | number |  |
| `stateCode` | string |  |
| `stateName` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/FemaWebDisasterDeclarations` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-fema-web-disaster-declarations.md) for the provider-specific parameters and requirements.

