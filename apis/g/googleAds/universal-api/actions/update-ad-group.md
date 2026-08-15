# Google Ads: Update Ad Group

Updates an existing ad group in Google Ads.

```
PUT https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/update-ad-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/update-ad-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "1234567890",
  "operations[]": [
    {}
  ],
  "operations[].update.resourceName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/update-ad-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "1234567890",
    "operations[]": [{}],
    "operations[].update.resourceName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | list | yes | Example: `1234567890`. |
| `operations[]` | array<object> | yes | List of mutate operations. |
| `operations[].update` | object | no | Update payload for each mutate operation. |
| `operations[].update.cpcBidMicros` | number | no |  |
| `operations[].update.name` | string | no |  |
| `operations[].update.resourceName` | string | yes |  |
| `operations[].update.status` | list | no | One of: `ENABLED`, `PAUSED`, `REMOVED`, `UNKNOWN`, `UNSPECIFIED`. |
| `operations[].updateMask` | string | no | Default: `name,status,cpc_bid_micros`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `partialFailure` | boolean | no | Default: `false`. |
| `responseContentType` | list | no | One of: `MUTABLE_RESOURCE`, `RESOURCE_NAME_ONLY`, `UNSPECIFIED`. Default: `RESOURCE_NAME_ONLY`. |
| `validateOnly` | boolean | no | Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "resourceName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resourceName` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/adGroups:mutate` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ad-group.md) for the provider-specific parameters and requirements.

