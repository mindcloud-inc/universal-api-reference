# Sonderplan: Get Groups



```
GET https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sonderplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-groups?${params}`, {
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
      "aclAdmin": "string",
      "aclProject": "string",
      "aclSchedule": "string",
      "description": "string",
      "id": 1,
      "isDefault": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aclAdmin` | string |  |
| `aclProject` | string |  |
| `aclSchedule` | string |  |
| `description` | string |  |
| `id` | number |  |
| `isDefault` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Sonderplan API, this operation is `GET /group` (base URL `https://api.sonderplan.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-groups.md) for the provider-specific parameters and requirements.

