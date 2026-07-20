# HoneyHive: Get Datasets

Retrieves a list of datasets from HoneyHive.

```
GET https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-datasets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoneyHive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-datasets?connectionId=$CONNECTION_ID&project=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-datasets?${params}`, {
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
| `project` | string | yes | Project name associated with datasets. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "testcases": [
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
| `testcases` | array<object> |  |

## Native endpoint

Through the native HoneyHive API, this operation is `GET /datasets` (base URL `https://api.honeyhive.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-datasets.md) for the provider-specific parameters and requirements.

