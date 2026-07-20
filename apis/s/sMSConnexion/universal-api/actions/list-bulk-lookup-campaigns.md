# SMS Connexion: List Bulk Lookup Campaigns

Retrieves bulk lookup campaigns from SMS Connexion.

```
GET https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/list-bulk-lookup-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/list-bulk-lookup-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/list-bulk-lookup-campaigns?${params}`, {
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
      "data": [
        "string"
      ],
      "datetimeAdded": "string",
      "id": "string",
      "totalCost": 1,
      "totalPhoneNumbers": 1,
      "totalValid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array |  |
| `datetimeAdded` | string |  |
| `id` | string |  |
| `totalCost` | number |  |
| `totalPhoneNumbers` | number |  |
| `totalValid` | number |  |

## Native endpoint

Through the native SMS Connexion API, this operation is `GET /numbers/lookup` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bulk-lookup-campaigns.md) for the provider-specific parameters and requirements.

