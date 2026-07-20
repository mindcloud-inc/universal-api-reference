# Weights & Biases: Get Projects Info

Retrieves project identifiers from Weights & Biases.

```
GET https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/get-projects-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weights & Biases `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/get-projects-info?connectionId=$CONNECTION_ID&project_ids%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_ids[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/get-projects-info?${params}`, {
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
| `project_ids[]` | array<string> | yes | External W&B project IDs in entity/project format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "external_project_id": "string",
      "internal_project_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `external_project_id` | string | External project ID in entity/project format. |
| `internal_project_id` | string | Internal W&B project identifier. |

## Native endpoint

Through the native Weights & Biases API, this operation is `POST /service/projects_info` (base URL `https://trace.wandb.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-projects-info.md) for the provider-specific parameters and requirements.

