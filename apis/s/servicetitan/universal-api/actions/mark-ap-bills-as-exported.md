# ServiceTitan: Mark AP Bills as Exported



```
PUT https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/mark-ap-bills-as-exported
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/mark-ap-bills-as-exported" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "billIds[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/mark-ap-bills-as-exported', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "billIds[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billIds[]` | array<number> | yes | AP bill IDs to mark as exported. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `POST accounting/v2/tenant/{{credentials.tenant}}/ap-bills/markasexported` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-ap-bills-as-exported.md) for the provider-specific parameters and requirements.

