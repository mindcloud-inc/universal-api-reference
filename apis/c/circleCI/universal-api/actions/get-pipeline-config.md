# CircleCI: Get Pipeline Config



```
GET https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-pipeline-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-pipeline-config?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-pipeline-config?${params}`, {
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
      "compiled": "string",
      "setupConfig": true,
      "source": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `compiled` | string |  |
| `setupConfig` | boolean |  |
| `source` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `GET /pipeline/:pipeline_id/config` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pipeline-config.md) for the provider-specific parameters and requirements.

