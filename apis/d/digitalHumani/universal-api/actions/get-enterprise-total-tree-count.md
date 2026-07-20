# Digital Humani: Get Enterprise Total Tree Count

Retrieves an enterprise's total tree count from Digital Humani.

```
GET https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/get-enterprise-total-tree-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Humani `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/get-enterprise-total-tree-count?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/get-enterprise-total-tree-count?${params}`, {
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
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |

## Native endpoint

Through the native Digital Humani API, this operation is `GET /enterprise/:id/treeCount/total` (base URL `https://api.digitalhumani.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-enterprise-total-tree-count.md) for the provider-specific parameters and requirements.

