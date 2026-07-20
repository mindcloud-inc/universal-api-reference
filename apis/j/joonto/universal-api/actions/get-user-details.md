# Joonto: Get User Details



```
GET https://connect.mindcloud.co/v1/universal/joonto/latest/actions/get-user-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Joonto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joonto/latest/actions/get-user-details?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/joonto/latest/actions/get-user-details?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": 1,
      "active": true,
      "connectedToGoogle": true,
      "connectedToOutlook": true,
      "count": 1,
      "dateCreated": "string",
      "email": "ava@example.com",
      "extension": "string",
      "id": 1,
      "imageId": 1,
      "isJoontoAdmin": true,
      "joontoPhone": "string",
      "joontoPhonePretty": "string",
      "locked": true,
      "mainAccount": 1,
      "name": "Ava Chen",
      "phone": "string",
      "phonePretty": "string",
      "phoneVerified": true,
      "plan": "string",
      "roles": "string",
      "scheduleId": 1,
      "timeZone": "string",
      "timeZoneFriendly": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | number |  |
| `active` | boolean |  |
| `connectedToGoogle` | boolean |  |
| `connectedToOutlook` | boolean |  |
| `count` | number |  |
| `dateCreated` | string |  |
| `email` | string |  |
| `extension` | string |  |
| `id` | number |  |
| `imageId` | number |  |
| `isJoontoAdmin` | boolean |  |
| `joontoPhone` | string |  |
| `joontoPhonePretty` | string |  |
| `locked` | boolean |  |
| `mainAccount` | number |  |
| `name` | string |  |
| `phone` | string |  |
| `phonePretty` | string |  |
| `phoneVerified` | boolean |  |
| `plan` | string |  |
| `roles` | string |  |
| `scheduleId` | number |  |
| `timeZone` | string |  |
| `timeZoneFriendly` | string |  |

## Native endpoint

Through the native Joonto API, this operation is `GET /api/Users/Get/:id` (base URL `https://api.joonto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-details.md) for the provider-specific parameters and requirements.

