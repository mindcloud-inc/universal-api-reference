# ECI Bolt: List Stages



```
GET https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-stages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECI Bolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-stages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-stages?${params}`, {
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
      "description": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | number |  |

## Native endpoint

Through the native ECI Bolt API, this operation is `GET /open/v1/stages` (base URL `https://app.bolttech.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stages.md) for the provider-specific parameters and requirements.

