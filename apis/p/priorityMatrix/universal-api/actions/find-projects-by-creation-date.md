# Priority Matrix: Find Projects By Creation Date

Finds Priority Matrix projects by creation date.

```
GET https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/find-projects-by-creation-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority Matrix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/find-projects-by-creation-date?connectionId=$CONNECTION_ID&limit=25&offset=0&creationDateGt=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "creationDateGt": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/find-projects-by-creation-date?${params}`, {
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
| `creationDateGt` | number | yes | Creation date lower bound as epoch seconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationDate": 1,
      "idd": 1,
      "name": "Ava Chen",
      "resource_uri": "string",
      "state": 1,
      "webLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationDate` | number |  |
| `idd` | number |  |
| `name` | string |  |
| `resource_uri` | string |  |
| `state` | number |  |
| `webLink` | string |  |

## Native endpoint

Through the native Priority Matrix API, this operation is `GET /api/v1/project/` (base URL `https://sync.appfluence.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/find-projects-by-creation-date.md) for the provider-specific parameters and requirements.

