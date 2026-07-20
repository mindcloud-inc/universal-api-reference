# GMass: List Campaigns For Zapier

Retrieves GMass campaigns available for Zapier.

```
GET https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-campaigns-for-zapier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GMass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-campaigns-for-zapier?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-campaigns-for-zapier?${params}`, {
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
      "CampaignSubject": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CampaignSubject` | string | Campaign subject line. |
| `id` | number | GMass campaign ID. |

## Native endpoint

Through the native GMass API, this operation is `GET /campaigns/zapier` (base URL `https://api.gmass.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns-for-zapier.md) for the provider-specific parameters and requirements.

