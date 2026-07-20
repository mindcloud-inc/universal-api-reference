# Habitica: List In-App Rewards

Retrieves in-app rewards from Habitica.

```
GET https://connect.mindcloud.co/v1/universal/habitica/latest/actions/list-in-app-rewards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Habitica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/habitica/latest/actions/list-in-app-rewards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/habitica/latest/actions/list-in-app-rewards?${params}`, {
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
      "currency": "string",
      "isSuggested": true,
      "key": "string",
      "klass": "string",
      "notes": "string",
      "pinType": "string",
      "set": "string",
      "text": "string",
      "type": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `isSuggested` | boolean |  |
| `key` | string |  |
| `klass` | string |  |
| `notes` | string |  |
| `pinType` | string |  |
| `set` | string |  |
| `text` | string |  |
| `type` | string |  |
| `value` | number |  |

## Native endpoint

Through the native Habitica API, this operation is `GET /user/in-app-rewards` (base URL `https://habitica.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-in-app-rewards.md) for the provider-specific parameters and requirements.

