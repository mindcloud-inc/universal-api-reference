# Flatfile: Create Job

Creates a new job in Flatfile.

```
POST https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flatfile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "operation": "submitActionFg",
  "source": {
    "spaceId": "us_spc_mindcloud_flatfile"
  },
  "type": "workbook"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "operation": "submitActionFg",
    "source": {"spaceId":"us_spc_mindcloud_flatfile"},
    "type": "workbook"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `operation` | string | yes | Job operation. Default: `submitActionFg`. |
| `source` | string | yes | Job source descriptor. Default: `{"spaceId":"us_spc_mindcloud_flatfile"}`. |
| `type` | string | yes | Job type. Default: `workbook`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Created job payload. |

## Native endpoint

Through the native Flatfile API, this operation is `POST /jobs` (base URL `https://api.x.flatfile.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

