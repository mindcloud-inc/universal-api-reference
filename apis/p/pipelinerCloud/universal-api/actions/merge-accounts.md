# Pipeliner Cloud: Merge Accounts

Merges existing accounts in Pipeliner Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/pipelinerCloud/latest/actions/merge-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeliner Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pipelinerCloud/latest/actions/merge-accounts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipelinerCloud/latest/actions/merge-accounts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Merged account ID. |
| `name` | string | Merged account name. |

## Native endpoint

Through the native Pipeliner Cloud API, this operation is `POST /entities/Accounts/merge` (base URL `{{credentials.serviceUrl}}/api/v100/rest/spaces/{{credentials.spaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-accounts.md) for the provider-specific parameters and requirements.

