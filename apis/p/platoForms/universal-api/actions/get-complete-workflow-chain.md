# PlatoForms: Get Complete Workflow Chain

Retrieves a complete workflow chain from PlatoForms.

```
GET https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-complete-workflow-chain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlatoForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-complete-workflow-chain?connectionId=$CONNECTION_ID&workflow_identifier=string&submission_identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflow_identifier": "string",
  "submission_identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-complete-workflow-chain?${params}`, {
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
| `workflow_identifier` | string | yes |  |
| `submission_identifier` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `page` | number |  |
| `results_per_page` | number |  |
| `submissions` | object |  |
| `total_count` | number |  |
| `total_pages` | number |  |

## Native endpoint

Through the native PlatoForms API, this operation is `GET /workflow/{{workflow_identifier}}/submission/{{submission_identifier}}/` (base URL `https://api.platoforms.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-complete-workflow-chain.md) for the provider-specific parameters and requirements.

