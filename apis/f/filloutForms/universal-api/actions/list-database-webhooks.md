# Fillout Forms: List Database Webhooks

Retrieves database webhooks from Fillout.

```
GET https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/list-database-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/list-database-webhooks?connectionId=$CONNECTION_ID&databaseId=base_abc123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "base_abc123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/list-database-webhooks?${params}`, {
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
| `databaseId` | string | yes | The unique identifier of the database. Example: `base_abc123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "webhooks": [
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
| `webhooks` | array<object> | Configured database webhooks. |

## Native endpoint

Through the native Fillout Forms API, this operation is `GET https://tables.fillout.com/api/v1/bases/:databaseId/webhooks` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-database-webhooks.md) for the provider-specific parameters and requirements.

