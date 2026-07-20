# Oneflow: List Workspaces

Retrieves workspaces from Oneflow.

```
GET https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oneflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-workspaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-workspaces?${params}`, {
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
      "_integration_permissions": [
        {}
      ],
      "_links": {},
      "_permissions": {},
      "company_name": "Ava Chen",
      "country_code": "string",
      "created_time": "string",
      "date_format": "string",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "registration_number": "string",
      "type": "string",
      "updated_time": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_integration_permissions` | array<object> | Integration permissions available for the workspace. |
| `_links` | object | Links related to the workspace resource. |
| `_permissions` | object | Permission flags for the workspace. |
| `company_name` | string | The workspace company name. |
| `country_code` | string | The workspace country code. |
| `created_time` | string | When the workspace was created. |
| `date_format` | string | The workspace date format. |
| `description` | string | The workspace description. |
| `id` | number | The Oneflow workspace ID. |
| `name` | string | The workspace name. |
| `registration_number` | string | The workspace registration number. |
| `type` | string | The workspace type. |
| `updated_time` | string | When the workspace was last updated. |

## Native endpoint

Through the native Oneflow API, this operation is `GET /workspaces` (base URL `https://api.oneflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

