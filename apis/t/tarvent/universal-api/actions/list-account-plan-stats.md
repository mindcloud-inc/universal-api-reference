# Tarvent: List Account Plan Stats

Retrieves account plan stats from Tarvent.

```
GET https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/list-account-plan-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tarvent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/list-account-plan-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/list-account-plan-stats?${params}`, {
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
      "engagementScore": 1,
      "id": "string",
      "itemCount": 1,
      "senderReputation": 1,
      "storageBytes": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `engagementScore` | number |  |
| `id` | string |  |
| `itemCount` | number |  |
| `senderReputation` | number |  |
| `storageBytes` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Tarvent API, this operation is `POST /graphql` (base URL `https://api.tarvent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-account-plan-stats.md) for the provider-specific parameters and requirements.

