# Zoho Projects: List Portals

Retrieves portals from Zoho Projects.

```
GET https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/list-portals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/list-portals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/list-portals?${params}`, {
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
      "bugPlan": "string",
      "id": "string",
      "isDefaultPortal": true,
      "orgLogo": "string",
      "orgName": "Ava Chen",
      "owner": {
        "businessHoursId": "string",
        "email": "ava@example.com",
        "firstName": "Ava",
        "fullName": "Ava Chen",
        "id": "string",
        "isClientUser": true,
        "lastName": "Chen",
        "name": "Ava Chen",
        "zpuid": "string"
      },
      "portalName": "Ava Chen",
      "portalOwner": "string",
      "portalType": "string",
      "portalUrl": "https://example.com",
      "profile": {
        "id": "string",
        "name": "Ava Chen"
      },
      "profileId": "string",
      "projectPlan": "string",
      "timezone": "string",
      "zsoid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bugPlan` | string |  |
| `id` | string |  |
| `isDefaultPortal` | boolean |  |
| `orgLogo` | string |  |
| `orgName` | string |  |
| `owner.businessHoursId` | string |  |
| `owner.email` | string |  |
| `owner.firstName` | string |  |
| `owner.fullName` | string |  |
| `owner.id` | string |  |
| `owner.isClientUser` | boolean |  |
| `owner.lastName` | string |  |
| `owner.name` | string |  |
| `owner.zpuid` | string |  |
| `portalName` | string |  |
| `portalOwner` | string |  |
| `portalType` | string |  |
| `portalUrl` | string |  |
| `profile.id` | string |  |
| `profile.name` | string |  |
| `profileId` | string |  |
| `projectPlan` | string |  |
| `timezone` | string |  |
| `zsoid` | string |  |

## Native endpoint

Through the native Zoho Projects API, this operation is `GET /portals` (base URL `https://projectsapi.zoho.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-portals.md) for the provider-specific parameters and requirements.

