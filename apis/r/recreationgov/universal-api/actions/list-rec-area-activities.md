# Recreation.gov: List Rec Area Activities

Retrieves activities for a recreation area from Recreation.gov.

```
GET https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/list-rec-area-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recreation.gov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/list-rec-area-activities?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/list-rec-area-activities?${params}`, {
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
| `id` | number | yes |  |
| `query` | string | no | Filter activities by name. |
| `limit` | number | no | Maximum number of records to return. |
| `offset` | number | no | Number of records to skip before returning results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActivityID": 1,
      "ActivityLevel": 1,
      "ActivityName": "Ava Chen",
      "ActivityParentID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActivityID` | number |  |
| `ActivityLevel` | number |  |
| `ActivityName` | string |  |
| `ActivityParentID` | number |  |

## Native endpoint

Through the native Recreation.gov API, this operation is `GET /recareas/{id}/activities` (base URL `https://ridb.recreation.gov/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-rec-area-activities.md) for the provider-specific parameters and requirements.

