# UpGuard: List Vendor Domains

Retrieves domains for a monitored vendor in UpGuard.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-vendor-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-vendor-domains?connectionId=$CONNECTION_ID&limit=25&offset=0&vendorPrimaryHostname=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "vendorPrimaryHostname": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-vendor-domains?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vendorPrimaryHostname` | string | yes | The primary hostname of the vendor to list domains for. |
| `active` | boolean | no | Include active domains. Default: `true`. |
| `inactive` | boolean | no | Include inactive domains. Default: `true`. |
| `labels[]` | array<string> | no | Filter domains by the provided labels. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domains": [
        {
          "active": true,
          "hostname": "Ava Chen",
          "primaryDomain": true
        }
      ],
      "nextPageToken": "string",
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domains[].active` | boolean |  |
| `domains[].hostname` | string |  |
| `domains[].primaryDomain` | boolean |  |
| `nextPageToken` | string |  |
| `totalResults` | number |  |

## Native endpoint

Through the native UpGuard API, this operation is `GET /vendor/domains` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-vendor-domains.md) for the provider-specific parameters and requirements.

