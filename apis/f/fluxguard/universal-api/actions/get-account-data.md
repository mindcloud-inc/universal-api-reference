# Fluxguard: Get Account Data

Retrieves your Fluxguard account attributes.

```
GET https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/get-account-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluxguard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/get-account-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/get-account-data?${params}`, {
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
      "created": 1,
      "credits": 1,
      "flags": {},
      "id": "string",
      "lastFreeCredits": 1,
      "lastTouch": 1,
      "notifyGap": 1,
      "plan": 1,
      "siteCount": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number | Account creation timestamp in milliseconds. |
| `credits` | number | Remaining account credits. |
| `flags` | object | Account status flag definitions. |
| `id` | string | Fluxguard account identifier. |
| `lastFreeCredits` | number | Timestamp of the last free credits event in milliseconds. |
| `lastTouch` | number | Timestamp of the last account activity in milliseconds. |
| `notifyGap` | number | Notification gap setting. |
| `plan` | number | Plan identifier. |
| `siteCount` | number | Number of monitored sites in the account. |
| `status` | string | Current account status. |

## Native endpoint

Through the native Fluxguard API, this operation is `GET /account` (base URL `https://api.fluxguard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-data.md) for the provider-specific parameters and requirements.

