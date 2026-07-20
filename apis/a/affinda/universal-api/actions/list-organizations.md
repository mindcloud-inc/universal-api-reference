# Affinda: List Organizations

Retrieves all accessible organizations from Affinda.

```
GET https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Affinda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-organizations?${params}`, {
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
      "avatar": "string",
      "awsMarketplaceLink": "https://example.com",
      "id": 1,
      "identifier": "string",
      "isTrial": true,
      "name": "Ava Chen",
      "resthookSignatureKey": "string",
      "showCustomFieldCreation": true,
      "userRole": "string",
      "usesPortalV3": true,
      "validationToolConfig": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string |  |
| `awsMarketplaceLink` | string |  |
| `id` | number |  |
| `identifier` | string |  |
| `isTrial` | boolean |  |
| `name` | string |  |
| `resthookSignatureKey` | string |  |
| `showCustomFieldCreation` | boolean |  |
| `userRole` | string |  |
| `usesPortalV3` | boolean |  |
| `validationToolConfig` | object |  |

## Native endpoint

Through the native Affinda API, this operation is `GET /v3/organizations` (base URL `https://api.us1.affinda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

