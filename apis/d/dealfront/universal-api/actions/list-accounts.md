# Dealfront: List Accounts

Retrieves accounts from Dealfront.

```
GET https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dealfront `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/list-accounts?${params}`, {
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
      "attributes": {
        "name": "Ava Chen",
        "onTrial": true,
        "subscription": "string",
        "subscriptionAddons": [
          "string"
        ],
        "timezone": "string",
        "websiteTrackingStatus": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.name` | string |  |
| `attributes.onTrial` | boolean |  |
| `attributes.subscription` | string |  |
| `attributes.subscriptionAddons[]` | string |  |
| `attributes.timezone` | string |  |
| `attributes.websiteTrackingStatus` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Dealfront API, this operation is `GET /accounts` (base URL `https://api.leadfeeder.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.

