# AdvantShop: Get Bonus Card Settings

Retrieves bonus card settings from AdvantShop.

```
GET https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/get-bonus-card-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AdvantShop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/get-bonus-card-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/get-bonus-card-settings?${params}`, {
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
      "bonusFirstPercent": 1,
      "bonusPercent": 1,
      "isEnabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bonusFirstPercent` | number |  |
| `bonusPercent` | number |  |
| `isEnabled` | boolean |  |

## Native endpoint

Through the native AdvantShop API, this operation is `GET /bonus-cards/settings` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bonus-card-settings.md) for the provider-specific parameters and requirements.

