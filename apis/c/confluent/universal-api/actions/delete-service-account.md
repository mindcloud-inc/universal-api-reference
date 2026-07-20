# Confluent: Delete Service Account

Deletes an existing service account from Confluent Cloud.

```
DELETE https://connect.mindcloud.co/v1/universal/confluent/latest/actions/delete-service-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/confluent/latest/actions/delete-service-account?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/confluent/latest/actions/delete-service-account?${params}`, {
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
| `id` | string | yes | The unique identifier for the service account. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Confluent API, this operation is `DELETE /iam/v2/service-accounts/:id` (base URL `https://api.confluent.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-service-account.md) for the provider-specific parameters and requirements.

