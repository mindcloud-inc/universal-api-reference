# Weights & Biases: Read Object

Retrieves an object version from Weights & Biases.

```
GET https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/read-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weights & Biases `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/read-object?connectionId=$CONNECTION_ID&digest=string&object_id=string&project_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "digest": "string",
  "object_id": "string",
  "project_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/read-object?${params}`, {
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
| `digest` | string | yes | The object version digest to read. |
| `object_id` | string | yes | The W&B Weave object ID to read. |
| `project_id` | string | yes | W&B project identifier in entity/project format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "obj": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `obj` | object | Object version metadata and value for the requested object digest. |

## Native endpoint

Through the native Weights & Biases API, this operation is `POST /obj/read` (base URL `https://trace.wandb.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-object.md) for the provider-specific parameters and requirements.

