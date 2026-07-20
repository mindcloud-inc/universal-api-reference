# ShipWise: Get Best Email Preference IDs V2

Retrieves recommended email preference IDs from ShipWise.

```
GET https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/get-best-email-preference-ids-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShipWise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/get-best-email-preference-ids-v2?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/get-best-email-preference-ids-v2?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ShipWise API returns.

## Native endpoint

Through the native ShipWise API, this operation is `GET /api/v2/Settings/GetBestEmailPreferenceIds` (base URL `https://api.shipwise.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-best-email-preference-ids-v2.md) for the provider-specific parameters and requirements.

