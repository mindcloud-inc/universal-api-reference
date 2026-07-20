# ServiceTitan: List Reports

Retrieves reports from ServiceTitan by category.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-reports?connectionId=$CONNECTION_ID&limit=25&offset=0&reportCategory=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "reportCategory": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-reports?${params}`, {
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
| `reportCategory` | string | yes | ID of category taken from the category list endpoint. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeTotal` | boolean | no | Whether total count should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Report description. |
| `id` | number | Report identifier within the category. |
| `name` | string | Report display name. |

## Native endpoint

Through the native ServiceTitan API, this operation is `GET reporting/v2/tenant/{{credentials.tenant}}/report-category/:report_category/reports` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-reports.md) for the provider-specific parameters and requirements.

