# Teamwork Projects: List Notebooks

Retrieves all notebooks from Teamwork Projects.

```
GET https://connect.mindcloud.co/v1/universal/teamworkProjects/latest/actions/list-notebooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamwork Projects `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamworkProjects/latest/actions/list-notebooks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamworkProjects/latest/actions/list-notebooks?${params}`, {
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
      "included": {},
      "meta": {},
      "notebooks": [
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
| `included` | object | Included related resources keyed by type. |
| `meta` | object | Pagination metadata. |
| `notebooks` | array<object> | Teamwork notebook records. |

## Native endpoint

Through the native Teamwork Projects API, this operation is `GET /notebooks.json` (base URL `{{credentials.accessTokenRequest.installation.apiEndPoint}}projects/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-notebooks.md) for the provider-specific parameters and requirements.

