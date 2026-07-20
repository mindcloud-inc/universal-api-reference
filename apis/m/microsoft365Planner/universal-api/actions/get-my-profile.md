# Microsoft 365 Planner: Get My Profile



```
GET https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/get-my-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/get-my-profile?${params}`, {
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
      "businessPhones": [
        "string"
      ],
      "displayName": "Ava Chen",
      "givenName": "Ava Chen",
      "id": "string",
      "jobTitle": "string",
      "mail": "string",
      "mobilePhone": "string",
      "officeLocation": "string",
      "preferredLanguage": "string",
      "surname": "Ava Chen",
      "userPrincipalName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessPhones` | array<string> |  |
| `displayName` | string |  |
| `givenName` | string |  |
| `id` | string |  |
| `jobTitle` | string |  |
| `mail` | string |  |
| `mobilePhone` | string |  |
| `officeLocation` | string |  |
| `preferredLanguage` | string |  |
| `surname` | string |  |
| `userPrincipalName` | string |  |

## Native endpoint

Through the native Microsoft 365 Planner API, this operation is `GET /v1.0/me` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-profile.md) for the provider-specific parameters and requirements.

