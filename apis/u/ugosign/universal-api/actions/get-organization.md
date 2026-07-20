# Ugosign: Get Organization

Retrieves an organization summary from Ugosign.

```
GET https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ugosign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/get-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/get-organization?${params}`, {
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
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "extraStorageGb": 1,
      "id": "string",
      "identityTokens": 1,
      "locale": "string",
      "overrunProtection": true,
      "slug": "string",
      "smsTokens": 1,
      "taxPercentage": "string",
      "title": "string",
      "trialEndsAt": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `createdAt` | date |  |
| `extraStorageGb` | number |  |
| `id` | string |  |
| `identityTokens` | number |  |
| `locale` | string |  |
| `overrunProtection` | boolean |  |
| `slug` | string |  |
| `smsTokens` | number |  |
| `taxPercentage` | string |  |
| `title` | string |  |
| `trialEndsAt` | date |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Ugosign API, this operation is `GET /v1/organization` (base URL `https://app.ugosign.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

