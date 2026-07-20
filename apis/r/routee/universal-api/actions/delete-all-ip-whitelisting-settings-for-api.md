# Routee: Delete all IP whitelisting settings for API

Deletes all API IP whitelisting settings from Routee.

```
DELETE https://connect.mindcloud.co/v1/universal/routee/latest/actions/delete-all-ip-whitelisting-settings-for-api
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/routee/latest/actions/delete-all-ip-whitelisting-settings-for-api?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/delete-all-ip-whitelisting-settings-for-api?${params}`, {
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
      "whitelistedIps": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `whitelistedIps[]` | array<string> |  |

## Native endpoint

Through the native Routee API, this operation is `DELETE /security/whitelist` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-all-ip-whitelisting-settings-for-api.md) for the provider-specific parameters and requirements.

