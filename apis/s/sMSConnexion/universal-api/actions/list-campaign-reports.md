# SMS Connexion: List Campaign Reports

Retrieves sent campaigns from SMS Connexion.

```
GET https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/list-campaign-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/list-campaign-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/list-campaign-reports?${params}`, {
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
      "accepted": 1,
      "channel": "string",
      "cost": 1,
      "data": [
        "string"
      ],
      "datetimeAdded": "string",
      "delivered": 1,
      "failed": 1,
      "from": "string",
      "groups": [
        "string"
      ],
      "id": "string",
      "info": {},
      "name": "Ava Chen",
      "noCoverage": 1,
      "parts": 1,
      "phoneNumbers": 1,
      "scheduled": 1,
      "source": "string",
      "status": {},
      "text": "string",
      "totalCampaigns": 1,
      "totalPhoneNumers": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accepted` | number |  |
| `channel` | string |  |
| `cost` | number |  |
| `data` | array |  |
| `datetimeAdded` | string |  |
| `delivered` | number |  |
| `failed` | number |  |
| `from` | string |  |
| `groups` | array |  |
| `id` | string |  |
| `info` | object |  |
| `name` | string |  |
| `noCoverage` | number |  |
| `parts` | number |  |
| `phoneNumbers` | number |  |
| `scheduled` | number |  |
| `source` | string |  |
| `status` | object |  |
| `text` | string |  |
| `totalCampaigns` | number |  |
| `totalPhoneNumers` | number |  |

## Native endpoint

Through the native SMS Connexion API, this operation is `GET /reports/campaigns` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaign-reports.md) for the provider-specific parameters and requirements.

