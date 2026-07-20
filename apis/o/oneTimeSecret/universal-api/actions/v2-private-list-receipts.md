# One-Time Secret: Private List Receipts

Retrieves recent private secret receipts from One-Time Secret.

```
GET https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-private-list-receipts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a One-Time Secret `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-private-list-receipts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-private-list-receipts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "details": {},
      "records": [
        {}
      ],
      "shrimp": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of private receipt records returned. |
| `details` | object | Private list scope and grouping details. |
| `records` | array<object> | Recent private receipt records. |
| `shrimp` | string | Provider response marker when returned. |
| `user_id` | string | Authenticated user identifier when returned. |

## Native endpoint

Through the native One-Time Secret API, this operation is `GET /api/v2/private/recent` (base URL `https://us.onetimesecret.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v2-private-list-receipts.md) for the provider-specific parameters and requirements.

