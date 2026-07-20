# PlatoForms: List Form Submissions

Retrieves form submission metadata from PlatoForms.

```
GET https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/list-form-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlatoForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/list-form-submissions?connectionId=$CONNECTION_ID&form_identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "form_identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/list-form-submissions?${params}`, {
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
| `form_identifier` | string | yes |  |
| `sort` | string | no | Sort order (e.g., '-id' for newest first, '-submitted_date' for latest submissions) |
| `keywords` | string | no | Search keywords across searchable fields |
| `page` | number | no | Page number for pagination |
| `results_per_page` | number | no | Number of results per page |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "page": 1,
      "results_per_page": 1,
      "submissions": {},
      "total_count": 1,
      "total_pages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `page` | number |  |
| `results_per_page` | number |  |
| `submissions` | object |  |
| `total_count` | number |  |
| `total_pages` | number |  |

## Native endpoint

Through the native PlatoForms API, this operation is `GET /form/{{form_identifier}}/submissions/` (base URL `https://api.platoforms.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-submissions.md) for the provider-specific parameters and requirements.

