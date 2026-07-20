# HiDrive: Get Disabled Status

Retrieves the disabled status from HiDrive.

```
GET https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-disabled-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-disabled-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-disabled-status?${params}`, {
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
      "disabled": true,
      "reason": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `disabled` | boolean | Whether the account or feature is disabled. |
| `reason` | array<string> | Reasons for disabled state when present. |

## Native endpoint

Through the native HiDrive API, this operation is `GET /status/disabled` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-disabled-status.md) for the provider-specific parameters and requirements.

