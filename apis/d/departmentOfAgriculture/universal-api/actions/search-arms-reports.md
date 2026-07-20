# Department of Agriculture: Search ARMS Reports

Finds ARMS reports in Department of Agriculture by ID or name.

```
GET https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/search-arms-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Department of Agriculture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/search-arms-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/search-arms-reports?${params}`, {
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
| `id` | number | no | Filter reports by numeric report ID from the ARMS report list. |
| `name` | string | no | Filter reports by report name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "header": "string",
      "num": 1,
      "terms": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Report description, when supplied. |
| `header` | string | Report name. |
| `num` | number | ARMS report number. |
| `terms` | string | Provider search terms. |

## Native endpoint

Through the native Department of Agriculture API, this operation is `GET /arms/report` (base URL `https://api.ers.usda.gov/data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-arms-reports.md) for the provider-specific parameters and requirements.

