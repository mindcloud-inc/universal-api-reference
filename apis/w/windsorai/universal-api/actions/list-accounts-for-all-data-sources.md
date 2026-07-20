# Windsor.ai: List Accounts For All Data Sources

Retrieves connected accounts across all Windsor.ai data sources.

```
GET https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/list-accounts-for-all-data-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Windsor.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/list-accounts-for-all-data-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/list-accounts-for-all-data-sources?${params}`, {
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
      "accountId": "string",
      "accountName": "Ava Chen",
      "datasource": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string | Connected account identifier. |
| `accountName` | string | Connected account display name. |
| `datasource` | string | Windsor.ai datasource identifier. |
| `status` | string | Connected account status. |

## Native endpoint

Through the native Windsor.ai API, this operation is `GET /api/common/ds-accounts` (base URL `https://onboard.windsor.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-accounts-for-all-data-sources.md) for the provider-specific parameters and requirements.

