# Avalara AvaTax: Test Connection



```
GET https://connect.mindcloud.co/v1/universal/avalara/latest/actions/test-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avalara AvaTax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avalara/latest/actions/test-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avalara/latest/actions/test-connection?${params}`, {
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
      "authenticated": true,
      "authenticatedAccountId": 1,
      "authenticatedUserId": 1,
      "authenticatedUserName": "Ava Chen",
      "authenticationType": "string",
      "crmid": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticated` | boolean | Whether the request credentials were authenticated. |
| `authenticatedAccountId` | number | Authenticated AvaTax account ID. |
| `authenticatedUserId` | number | Authenticated AvaTax user ID. |
| `authenticatedUserName` | string | Authenticated AvaTax username. |
| `authenticationType` | string | Authentication mode used by AvaTax. |
| `crmid` | string | AvaTax CRM identifier. |
| `version` | string | AvaTax API version. |

## Native endpoint

Through the native Avalara AvaTax API, this operation is `GET utilities/ping` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-connection.md) for the provider-specific parameters and requirements.

