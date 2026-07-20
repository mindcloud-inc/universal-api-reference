# CircleCI: Get Pipeline Values



```
GET https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-pipeline-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-pipeline-values?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-pipeline-values?${params}`, {
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
| `pipeline_id` | string | no | Opaque pipeline identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branch": "string",
      "parameters": {},
      "tag": "string",
      "triggerParameters": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branch` | string |  |
| `parameters` | object |  |
| `tag` | string |  |
| `triggerParameters` | object |  |

## Native endpoint

Through the native CircleCI API, this operation is `GET /pipeline/:pipeline_id/values` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pipeline-values.md) for the provider-specific parameters and requirements.

