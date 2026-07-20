# TestDome: List Tests

Retrieves tests from TestDome.

```
GET https://connect.mindcloud.co/v1/universal/testDome/latest/actions/list-tests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TestDome `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testDome/latest/actions/list-tests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testDome/latest/actions/list-tests?${params}`, {
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
| `expand` | list<string> | no |  |
| `filterArchived` | string | no |  |
| `filterExcludeDeleted` | boolean | no |  |
| `filterHasQuestions` | boolean | no |  |
| `filterIsPublished` | boolean | no |  |
| `filterNotContainsQuestions` | list<number> | no |  |
| `filterTerm` | string | no |  |
| `select` | list<string> | no |  |
| `sort` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "hasMoreItems": true,
      "skip": 1,
      "top": 1,
      "totalCount": 1,
      "value": [
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
| `_links` | object | Dictionary |
| `hasMoreItems` | boolean |  |
| `skip` | number |  |
| `top` | number |  |
| `totalCount` | number |  |
| `value` | array<object> | TestModel[] |

## Native endpoint

Through the native TestDome API, this operation is `GET /tests` (base URL `https://api.staging.testdome.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tests.md) for the provider-specific parameters and requirements.

