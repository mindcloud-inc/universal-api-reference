# PagePixels: Create Website Domain Research Request



```
POST https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/create-website-domain-research-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PagePixels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/create-website-domain-research-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domains[]": [
    "string"
  ],
  "structures[0].data_type": "string",
  "structures[0].data_field_name": "Ava Chen",
  "structures[0].data_field_prompt_description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/create-website-domain-research-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domains[]": ["string"],
    "structures[0].data_type": "string",
    "structures[0].data_field_name": "Ava Chen",
    "structures[0].data_field_prompt_description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Name for this research job. |
| `additionalNotes` | string | no | Optional notes for the research job. |
| `domains[]` | array<string> | yes | List of domains to analyze. |
| `structures[0].data_type` | string | yes | The data type to extract for the first structure entry. |
| `structures[0].data_field_name` | string | yes | The result field name for the first structure entry. |
| `structures[0].data_field_prompt_description` | string | yes | The extraction prompt for the first structure entry. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string | The unique identifier for the created domain research job. |
| `status` | string | The initial job status returned by PagePixels. |

## Native endpoint

Through the native PagePixels API, this operation is `POST /api/domain_research_requests` (base URL `https://api.pagepixels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-website-domain-research-request.md) for the provider-specific parameters and requirements.

