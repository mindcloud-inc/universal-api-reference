# AdPage: Get Agency

Retrieves the current agency from AdPage.

```
GET https://connect.mindcloud.co/v1/universal/adPage/latest/actions/get-agency
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AdPage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adPage/latest/actions/get-agency?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adPage/latest/actions/get-agency?${params}`, {
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
      "cnameDomain": "Ava Chen",
      "complianceAccepted": true,
      "complianceAcceptedDate": {},
      "complianceUrl": {
        "url": "https://example.com"
      },
      "connectedEmail": true,
      "connectedStripe": true,
      "copyright": {},
      "darkColor": "string",
      "darkColorRGB": "string",
      "domain": "string",
      "enabledFunnelBuilder": true,
      "enabledRegister": true,
      "enabledWorkspaces": true,
      "enablePopupBuilder": true,
      "fifthColor": "string",
      "fifthColorRGB": "string",
      "fourthColor": "string",
      "fourthColorRGB": "string",
      "hero": "string",
      "icon": "string",
      "id": "string",
      "logo": "string",
      "name": "Ava Chen",
      "primaryColor": "string",
      "primaryColorRGB": "string",
      "projectDomain": "string",
      "secondaryColor": "string",
      "secondaryColorRGB": "string",
      "tagManagerId": "string",
      "takenSeats": 1,
      "usersNumber": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cnameDomain` | string |  |
| `complianceAccepted` | boolean |  |
| `complianceAcceptedDate` | object |  |
| `complianceUrl.url` | string |  |
| `connectedEmail` | boolean |  |
| `connectedStripe` | boolean |  |
| `copyright` | object |  |
| `darkColor` | string |  |
| `darkColorRGB` | string |  |
| `domain` | string |  |
| `enabledFunnelBuilder` | boolean |  |
| `enabledRegister` | boolean |  |
| `enabledWorkspaces` | boolean |  |
| `enablePopupBuilder` | boolean |  |
| `fifthColor` | string |  |
| `fifthColorRGB` | string |  |
| `fourthColor` | string |  |
| `fourthColorRGB` | string |  |
| `hero` | string |  |
| `icon` | string |  |
| `id` | string |  |
| `logo` | string |  |
| `name` | string |  |
| `primaryColor` | string |  |
| `primaryColorRGB` | string |  |
| `projectDomain` | string |  |
| `secondaryColor` | string |  |
| `secondaryColorRGB` | string |  |
| `tagManagerId` | string |  |
| `takenSeats` | number |  |
| `usersNumber` | number |  |

## Native endpoint

Through the native AdPage API, this operation is `GET /api/agency/` (base URL `https://whitelabel.adpage.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agency.md) for the provider-specific parameters and requirements.

