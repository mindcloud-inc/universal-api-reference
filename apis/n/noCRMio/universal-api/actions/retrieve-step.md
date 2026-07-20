# noCRM.io: Retrieve Step

Retrieves step details from noCRM.io.

```
GET https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/retrieve-step
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a noCRM.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/retrieve-step?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/retrieve-step?${params}`, {
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
| `id` | string | yes | Step ID or name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": 1,
      "name": "Ava Chen",
      "pipeline": {
        "createdAt": "string",
        "id": 1,
        "isDefault": true,
        "name": "Ava Chen",
        "updatedAt": "string"
      },
      "pipelineId": 1,
      "position": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | number |  |
| `name` | string |  |
| `pipeline` | object |  |
| `pipeline.createdAt` | string |  |
| `pipeline.id` | number |  |
| `pipeline.isDefault` | boolean |  |
| `pipeline.name` | string |  |
| `pipeline.updatedAt` | string |  |
| `pipelineId` | number |  |
| `position` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native noCRM.io API, this operation is `GET /steps/:id` (base URL `{{credentials.baseUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-step.md) for the provider-specific parameters and requirements.

