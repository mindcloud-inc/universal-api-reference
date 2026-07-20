# Dripcel: Opt Out Contact from Campaign

Updates a contact to opt out of one Dripcel campaign.

```
PUT https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/opt-out-contact-from-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dripcel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/opt-out-contact-from-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cell": "string",
  "campaignId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/opt-out-contact-from-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cell": "string",
    "campaignId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cell` | string | yes |  |
| `campaignId` | string | yes | The campaign ID to opt the contact out from. |
| `all` | boolean | no | Opt the contact out from all existing and future campaigns. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dripcel API returns.

## Native endpoint

Through the native Dripcel API, this operation is `PUT /contacts/:cell/optOut` (base URL `https://api.dripcel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/opt-out-contact-from-campaign.md) for the provider-specific parameters and requirements.

