# Intelliprint: Retrieve Print Job



```
GET https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/retrieve-print-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intelliprint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/retrieve-print-job?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/retrieve-print-job?${params}`, {
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
| `id` | string | yes | The Intelliprint print job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "confirmed": true,
      "created": 1,
      "id": "string",
      "object": "string",
      "reference": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `confirmed` | boolean |  |
| `created` | number |  |
| `id` | string |  |
| `object` | string |  |
| `reference` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Intelliprint API, this operation is `GET /prints/:id` (base URL `https://api.intelliprint.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-print-job.md) for the provider-specific parameters and requirements.

