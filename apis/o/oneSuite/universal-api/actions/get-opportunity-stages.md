# OneSuite: Get Opportunity Stages

Retrieves opportunity stages from OneSuite.

```
GET https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/get-opportunity-stages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/get-opportunity-stages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/get-opportunity-stages?${params}`, {
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
      "bgColor": "string",
      "borderColor": "string",
      "businessId": "string",
      "createdAt": "string",
      "darkColor": "string",
      "fgColor": "string",
      "id": "string",
      "isDefault": true,
      "isFolded": true,
      "lightColor": "string",
      "name": "Ava Chen",
      "sortId": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bgColor` | string |  |
| `borderColor` | string |  |
| `businessId` | string |  |
| `createdAt` | string |  |
| `darkColor` | string |  |
| `fgColor` | string |  |
| `id` | string |  |
| `isDefault` | boolean |  |
| `isFolded` | boolean |  |
| `lightColor` | string |  |
| `name` | string |  |
| `sortId` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native OneSuite API, this operation is `GET /v1/opportunities/stage` (base URL `https://api.onesuite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-opportunity-stages.md) for the provider-specific parameters and requirements.

