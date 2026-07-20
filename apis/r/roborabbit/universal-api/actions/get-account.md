# Roborabbit: Get Account

Retrieves account status and quota usage from Roborabbit.

```
GET https://connect.mindcloud.co/v1/universal/roborabbit/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Roborabbit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/roborabbit/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/roborabbit/latest/actions/get-account?${params}`, {
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
      "apiQuota": 1,
      "apiUsage": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "plan": "string",
      "uid": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiQuota` | number |  |
| `apiUsage` | number |  |
| `createdAt` | date |  |
| `plan` | string |  |
| `uid` | string |  |
| `workspace` | string |  |

## Native endpoint

Through the native Roborabbit API, this operation is `GET /v1/account` (base URL `https://api.roborabbit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

