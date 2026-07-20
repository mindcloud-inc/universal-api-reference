# Ayrshare: Get User Profile Details

Retrieves user profile details from Ayrshare.

```
GET https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/get-user-profile-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/get-user-profile-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/get-user-profile-details?${params}`, {
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
      "activeSocialAccounts": [
        "string"
      ],
      "created": {},
      "email": "ava@example.com",
      "lastApiCall": "2026-05-07T12:00:00.000Z",
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "linkedSocialAccounts": [
        "https://example.com"
      ],
      "monthlyApiCalls": 1,
      "monthlyPostCount": 1,
      "monthlyPostQuota": 1,
      "nextUpdate": "2026-05-07T12:00:00.000Z",
      "refId": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeSocialAccounts` | array<string> | Connected active social accounts, when present. |
| `created` | object | Ayrshare account creation timestamp. |
| `email` | string | Account email when returned by Ayrshare. |
| `lastApiCall` | date | Most recent API call timestamp. |
| `lastUpdated` | date | Last profile update timestamp. |
| `linkedSocialAccounts` | array<string> | Linked social accounts, when present. |
| `monthlyApiCalls` | number | API calls used in the current month. |
| `monthlyPostCount` | number | Posts used in the current month. |
| `monthlyPostQuota` | number | Monthly post quota. |
| `nextUpdate` | date | Next scheduled profile data update. |
| `refId` | string | Ayrshare profile reference ID. |
| `title` | string | Profile title. |

## Native endpoint

Through the native Ayrshare API, this operation is `GET /user` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-profile-details.md) for the provider-specific parameters and requirements.

