# Invision Community: Get Community Info



```
GET https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-community-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invision Community `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-community-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-community-info?${params}`, {
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
      "communityName": "Ava Chen",
      "communityUrl": "https://example.com",
      "ipsApplications": [
        "Ava Chen"
      ],
      "ipsVersion": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `communityName` | string |  |
| `communityUrl` | string |  |
| `ipsApplications` | array<string> |  |
| `ipsVersion` | string |  |

## Native endpoint

Through the native Invision Community API, this operation is `GET /core/hello` (base URL `{{credentials.communityBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-community-info.md) for the provider-specific parameters and requirements.

