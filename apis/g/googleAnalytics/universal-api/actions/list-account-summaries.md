# Google Analytics: List Account Summaries



```
GET https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/list-account-summaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Analytics `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/list-account-summaries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/list-account-summaries?${params}`, {
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
      "account": "string",
      "displayName": "Ava Chen",
      "name": "Ava Chen",
      "propertySummaries": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string | Account resource name, such as accounts/226916501 |
| `displayName` | string | Human-readable display name of the account |
| `name` | string | Account summary resource name, such as accountSummaries/226916501 |
| `propertySummaries` | array<object> | Property summaries under the account, each with property, displayName, propertyType, parent, and canEdit |

## Native endpoint

Through the native Google Analytics API, this operation is `GET https://analyticsadmin.googleapis.com/v1beta/accountSummaries` (base URL `https://analyticsdata.googleapis.com/v1beta`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-account-summaries.md) for the provider-specific parameters and requirements.

