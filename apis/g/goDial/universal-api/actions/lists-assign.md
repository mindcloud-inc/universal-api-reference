# GoDial: Assign Contact List to User

Assigns a contact list to a user in GoDial.

```
PUT https://connect.mindcloud.co/v1/universal/goDial/latest/actions/lists-assign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDial `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goDial/latest/actions/lists-assign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goDial/latest/actions/lists-assign', {
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
      "accountsId": "string",
      "id": "string",
      "listsId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountsId` | string |  |
| `id` | string |  |
| `listsId` | string |  |

## Native endpoint

Through the native GoDial API, this operation is `POST /externals/lists/assign` (base URL `https://enterprise.godial.cc/meta/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lists-assign.md) for the provider-specific parameters and requirements.

