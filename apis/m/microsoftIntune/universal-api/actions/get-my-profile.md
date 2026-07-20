# Microsoft Intune: Get My Profile

Retrieves the signed-in user profile from Microsoft Intune.

```
GET https://connect.mindcloud.co/v1/universal/microsoftIntune/latest/actions/get-my-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Intune `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftIntune/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftIntune/latest/actions/get-my-profile?${params}`, {
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
      "displayName": "Ava Chen",
      "id": "string",
      "jobTitle": "string",
      "mail": "string",
      "mobilePhone": "string",
      "officeLocation": "string",
      "userPrincipalName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string | User display name. |
| `id` | string | Microsoft Graph user ID. |
| `jobTitle` | string | User job title. |
| `mail` | string | Primary SMTP address when available. |
| `mobilePhone` | string | User mobile phone. |
| `officeLocation` | string | User office location. |
| `userPrincipalName` | string | User principal name. |

## Native endpoint

Through the native Microsoft Intune API, this operation is `GET /v1.0/me` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-profile.md) for the provider-specific parameters and requirements.

