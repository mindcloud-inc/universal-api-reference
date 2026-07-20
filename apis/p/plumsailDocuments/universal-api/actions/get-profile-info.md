# Plumsail Documents: Get Profile Info

Retrieves profile information from Plumsail Documents.

```
GET https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/get-profile-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plumsail Documents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/get-profile-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/get-profile-info?${params}`, {
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
      "email": "ava@example.com",
      "licenseInfo": {},
      "licenseStatus": "string",
      "name": "Ava Chen",
      "shortUserId": "string",
      "teamName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `licenseInfo` | object |  |
| `licenseStatus` | string |  |
| `name` | string |  |
| `shortUserId` | string |  |
| `teamName` | string |  |

## Native endpoint

Through the native Plumsail Documents API, this operation is `GET /api/v2/user/Profiles/me` (base URL `https://us-api.plumsail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profile-info.md) for the provider-specific parameters and requirements.

