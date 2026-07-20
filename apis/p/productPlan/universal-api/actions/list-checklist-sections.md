# ProductPlan: List Checklist Sections

Lists checklist sections for a launch in ProductPlan.

```
GET https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/list-checklist-sections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProductPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/list-checklist-sections?connectionId=$CONNECTION_ID&launchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "launchId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/list-checklist-sections?${params}`, {
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
| `launchId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "paging": {},
      "results": [
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
| `paging` | object | Pagination metadata for the response. |
| `results` | array<object> | Collection of records returned by this ProductPlan list endpoint. |

## Native endpoint

Through the native ProductPlan API, this operation is `GET /launches/:launch_id/checklist_sections` (base URL `https://app.productplan.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-checklist-sections.md) for the provider-specific parameters and requirements.

