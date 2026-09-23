# Google Analytics: List Accounts

Lists all Google Analytics accounts accessible to the connection.

```
GET https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/list-accounts?${params}`, {
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
| `pageSize` | number | no | Default: `50`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageToken` | string | no |  |
| `showDeleted` | boolean | no | Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTime": "string",
      "displayName": "Ava Chen",
      "name": "Ava Chen",
      "regionCode": "string",
      "updateTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTime` | string | Time the account was created |
| `displayName` | string | Human-readable display name of the account |
| `name` | string | Account resource name, such as accounts/226916501 |
| `regionCode` | string | Country region code associated with the account |
| `updateTime` | string | Time the account was last updated |

## Native endpoint

Through the native Google Analytics API, this operation is `GET https://analyticsadmin.googleapis.com/v1beta/accounts` (base URL `https://analyticsdata.googleapis.com/v1beta`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.

