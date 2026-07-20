# Webex Interact: Retrieve account metadata

Retrieves account metadata from Webex Interact.

```
GET https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/retrieve-account-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex Interact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/retrieve-account-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/retrieve-account-metadata?${params}`, {
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
      "account_balance": 1,
      "account_status": "string",
      "account_uid": "string",
      "created": "string",
      "default_currency": "string",
      "home_region": "string",
      "time_zone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_balance` | number |  |
| `account_status` | string |  |
| `account_uid` | string |  |
| `created` | string |  |
| `default_currency` | string |  |
| `home_region` | string |  |
| `time_zone` | string |  |

## Native endpoint

Through the native Webex Interact API, this operation is `GET /identity/v1/account` (base URL `https://api.webexinteract.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-account-metadata.md) for the provider-specific parameters and requirements.

