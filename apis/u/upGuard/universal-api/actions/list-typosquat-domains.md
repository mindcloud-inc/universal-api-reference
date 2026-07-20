# UpGuard: List Typosquat Domains

Retrieves typosquat domains from your UpGuard account.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-typosquat-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-typosquat-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-typosquat-domains?${params}`, {
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
      "domains": [
        {
          "addedAt": "string",
          "domain": "string",
          "lastScannedAt": "string",
          "numRegistered": 1,
          "numUnregistered": 1,
          "primaryDomain": true
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domains[].addedAt` | string |  |
| `domains[].domain` | string |  |
| `domains[].lastScannedAt` | string |  |
| `domains[].numRegistered` | number |  |
| `domains[].numUnregistered` | number |  |
| `domains[].primaryDomain` | boolean |  |

## Native endpoint

Through the native UpGuard API, this operation is `GET /typosquat` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-typosquat-domains.md) for the provider-specific parameters and requirements.

