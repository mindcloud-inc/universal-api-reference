# ManyReach: Get Prospect

Retrieves a prospect from ManyReach.

```
GET https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/get-prospect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/get-prospect?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/get-prospect?${params}`, {
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
| `id` | string | no | Prospect ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseListId": 1,
      "city": "string",
      "company": "string",
      "companySize": "string",
      "companySocial": "string",
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customImageUrl": "https://example.com",
      "domain": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "icebreaker": "string",
      "industry": "string",
      "jobPosition": "string",
      "lastName": "Chen",
      "location": "string",
      "logoUrl": "https://example.com",
      "notes": "string",
      "personalSocial": "string",
      "phone": "string",
      "prospectId": 1,
      "screenshotUrl": "https://example.com",
      "sendingActive": true,
      "sendingStatus": "string",
      "state": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseListId` | number |  |
| `city` | string |  |
| `company` | string |  |
| `companySize` | string |  |
| `companySocial` | string |  |
| `country` | string |  |
| `createdAt` | date |  |
| `customImageUrl` | string |  |
| `domain` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `icebreaker` | string |  |
| `industry` | string |  |
| `jobPosition` | string |  |
| `lastName` | string |  |
| `location` | string |  |
| `logoUrl` | string |  |
| `notes` | string |  |
| `personalSocial` | string |  |
| `phone` | string |  |
| `prospectId` | number |  |
| `screenshotUrl` | string |  |
| `sendingActive` | boolean |  |
| `sendingStatus` | string |  |
| `state` | string |  |
| `website` | string |  |

## Native endpoint

Through the native ManyReach API, this operation is `GET https://api.manyreach.com/api/v2/prospects/:id` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-prospect.md) for the provider-specific parameters and requirements.

