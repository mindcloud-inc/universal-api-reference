# Signaturit: Get Credits

Retrieves account credits from Signaturit.

```
GET https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/get-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Signaturit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/get-credits?${params}`, {
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
      "currentPeriod": {
        "from": "string",
        "to": "string"
      },
      "period": "string",
      "quantity": 1,
      "remainingCredits": 1,
      "type": "string",
      "usedCredits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPeriod.from` | string |  |
| `currentPeriod.to` | string |  |
| `period` | string |  |
| `quantity` | number |  |
| `remainingCredits` | number |  |
| `type` | string |  |
| `usedCredits` | number |  |

## Native endpoint

Through the native Signaturit API, this operation is `GET /account/credits.json` (base URL `https://api.sandbox.signaturit.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credits.md) for the provider-specific parameters and requirements.

