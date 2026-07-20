# Snapchat Ads: Update Ad Accounts

Updates existing ad accounts in Snapchat Ads.

```
PUT https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/update-ad-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/update-ad-accounts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string",
  "adAccounts": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/update-ad-accounts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string",
    "adAccounts": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes | The Snapchat Organization ID that owns the ad accounts to update. |
| `adAccounts` | list<object> | yes | An array of Snapchat ad account objects to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adaccounts": [
        {
          "adaccount": {
            "id": "string",
            "name": "Ava Chen",
            "status": "string"
          }
        }
      ],
      "request_id": "string",
      "request_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adaccounts[].adaccount.id` | string |  |
| `adaccounts[].adaccount.name` | string |  |
| `adaccounts[].adaccount.status` | string |  |
| `request_id` | string |  |
| `request_status` | string |  |

## Native endpoint

Through the native Snapchat Ads API, this operation is `PUT /organizations/:organizationId/adaccounts` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ad-accounts.md) for the provider-specific parameters and requirements.

