# smapOne: Get account stats

Retrieves account statistics from smapOne.

```
GET https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-account-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smapOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-account-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-account-stats?${params}`, {
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
      "categoryCount": 1,
      "dataCount": 1,
      "smapCount": 1,
      "subscriptionType": "string",
      "systemVersion": "string",
      "userCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryCount` | number |  |
| `dataCount` | number |  |
| `smapCount` | number |  |
| `subscriptionType` | string |  |
| `systemVersion` | string |  |
| `userCount` | number |  |

## Native endpoint

Through the native smapOne API, this operation is `GET /intern/Account/Stats` (base URL `https://platform.smapone.com/Backend`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-stats.md) for the provider-specific parameters and requirements.

