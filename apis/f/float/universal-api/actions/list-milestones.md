# Float: List Milestones

Retrieves milestones from Float.

```
GET https://connect.mindcloud.co/v1/universal/float/latest/actions/list-milestones
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/float/latest/actions/list-milestones?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/float/latest/actions/list-milestones?${params}`, {
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
      "created": "string",
      "date": "string",
      "endDate": "string",
      "milestoneId": 1,
      "modified": "string",
      "name": "Ava Chen",
      "phaseId": 1,
      "projectId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `date` | string |  |
| `endDate` | string |  |
| `milestoneId` | number |  |
| `modified` | string |  |
| `name` | string |  |
| `phaseId` | number |  |
| `projectId` | number |  |

## Native endpoint

Through the native Float API, this operation is `GET /milestones` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-milestones.md) for the provider-specific parameters and requirements.

