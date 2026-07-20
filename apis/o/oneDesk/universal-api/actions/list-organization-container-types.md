# OneDesk: List Organization Container Types

Retrieves organization container types from OneDesk.

```
GET https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/list-organization-container-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/list-organization-container-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/list-organization-container-types?${params}`, {
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
      "externalId": "string",
      "iconColor": 1,
      "iconStyleName": "Ava Chen",
      "isPortfolio": true,
      "label": "string",
      "visible": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `externalId` | string |  |
| `iconColor` | number |  |
| `iconStyleName` | string |  |
| `isPortfolio` | boolean |  |
| `label` | string |  |
| `visible` | boolean |  |

## Native endpoint

Through the native OneDesk API, this operation is `GET /rest/public/organization/containerTypes` (base URL `https://app.onedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-container-types.md) for the provider-specific parameters and requirements.

