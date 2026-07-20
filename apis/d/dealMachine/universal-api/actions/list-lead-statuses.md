# DealMachine: List Lead Statuses



```
GET https://connect.mindcloud.co/v1/universal/dealMachine/latest/actions/list-lead-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DealMachine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dealMachine/latest/actions/list-lead-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dealMachine/latest/actions/list-lead-statuses?${params}`, {
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
      "id": 1,
      "label": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `label` | string |  |

## Native endpoint

Through the native DealMachine API, this operation is `GET /public/v1/lead-statuses/` (base URL `https://api.dealmachine.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lead-statuses.md) for the provider-specific parameters and requirements.

