# QWIC: Get Data Source Training Status

Retrieves training status for a QWIC data source.

```
GET https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/get-data-source-training-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QWIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/get-data-source-training-status?connectionId=$CONNECTION_ID&sourceIds=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sourceIds": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/get-data-source-training-status?${params}`, {
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
| `sourceIds` | list<number> | yes | Comma-separated list of data source IDs. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native QWIC API, this operation is `GET /api/v1/ai/status/sources` (base URL `https://app.qwic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-source-training-status.md) for the provider-specific parameters and requirements.

