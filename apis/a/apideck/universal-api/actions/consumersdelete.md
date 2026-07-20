# Apideck: Delete consumer

Deletes a consumer and all their connections from Apideck Vault.

```
DELETE https://connect.mindcloud.co/v1/universal/apideck/latest/actions/consumersdelete
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apideck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/apideck/latest/actions/consumersdelete?connectionId=$CONNECTION_ID&consumer_id=%7B%7Bcredentials.consumerId%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "consumer_id": "{{credentials.consumerId}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apideck/latest/actions/consumersdelete?${params}`, {
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
| `consumer_id` | string | yes | Default: `{{credentials.consumerId}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object |  |

## Native endpoint

Through the native Apideck API, this operation is `DELETE /vault/consumers/:consumer_id` (base URL `https://unify.apideck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/consumersdelete.md) for the provider-specific parameters and requirements.

