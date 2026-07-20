# AMcards.com: Get User

Retrieves a specific user from AMcards.com.

```
GET https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AMcards.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/get-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | number | no | AMcards user identifier from the `/user/` resource URI. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressLine1": "string",
      "addressLine2": "string",
      "city": "string",
      "country": "string",
      "credits": 1,
      "dateJoined": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "lastTemplateUpdated": "2026-05-07T12:00:00.000Z",
      "phone": "string",
      "postage": {
        "bigcardCost": 1,
        "domesticCost": 1,
        "domesticCountries": [
          "string"
        ],
        "internationalCost": 1,
        "postcardCost": 1
      },
      "postal": "string",
      "resourceUri": "string",
      "showUpgradeMessage": true,
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressLine1` | string |  |
| `addressLine2` | string |  |
| `city` | string |  |
| `country` | string |  |
| `credits` | number |  |
| `dateJoined` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `lastTemplateUpdated` | date |  |
| `phone` | string |  |
| `postage.bigcardCost` | number |  |
| `postage.domesticCost` | number |  |
| `postage.domesticCountries[]` | string<string> |  |
| `postage.internationalCost` | number |  |
| `postage.postcardCost` | number |  |
| `postal` | string |  |
| `resourceUri` | string |  |
| `showUpgradeMessage` | boolean |  |
| `state` | string |  |

## Native endpoint

Through the native AMcards.com API, this operation is `GET /user/:userId/` (base URL `https://amcards.com/.api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

