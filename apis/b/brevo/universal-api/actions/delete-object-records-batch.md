# Brevo: Delete Object Records Batch



```
DELETE https://connect.mindcloud.co/v1/universal/brevo/latest/actions/delete-object-records-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/delete-object-records-batch?connectionId=$CONNECTION_ID&object_type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "object_type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/delete-object-records-batch?${params}`, {
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
| `object_type` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedCount": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedCount` | number |  |
| `message` | string |  |

## Native endpoint

Through the native Brevo API, this operation is `POST /v3/objects/:object_type/batch/delete` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-object-records-batch.md) for the provider-specific parameters and requirements.

