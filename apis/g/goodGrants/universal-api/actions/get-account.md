# Good Grants: Get account

Retrieves account details from Good Grants.

```
GET https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Good Grants `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/get-account?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "domains": [
        "string"
      ],
      "globalId": "string",
      "languages": [
        {}
      ],
      "name": "Ava Chen",
      "owner": {},
      "product": "string",
      "region": "string",
      "slug": "string",
      "timezone": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `domains` | array<string> |  |
| `globalId` | string |  |
| `languages` | array<object> |  |
| `name` | string |  |
| `owner` | object |  |
| `product` | string |  |
| `region` | string |  |
| `slug` | string |  |
| `timezone` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Good Grants API, this operation is `GET account` (base URL `https://api.cr4ce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

