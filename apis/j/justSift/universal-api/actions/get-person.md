# JustSift: Get Person



```
GET https://connect.mindcloud.co/v1/universal/justSift/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustSift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/justSift/latest/actions/get-person?connectionId=$CONNECTION_ID&idOrEmail=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrEmail": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/justSift/latest/actions/get-person?${params}`, {
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
| `idOrEmail` | string | yes | The person's Sift id or email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customPictureUrl": "https://example.com",
      "department": "string",
      "directoryId": "string",
      "directReportCount": 1,
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "isTeamLeader": true,
      "lastName": "Chen",
      "officialPictureUrl": "https://example.com",
      "pictureUrl": "https://example.com",
      "reportingPath": [
        "string"
      ],
      "teamLeaderId": "string",
      "title": "string",
      "totalReportCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customPictureUrl` | string | Custom profile picture URL. |
| `department` | string | Department. |
| `directoryId` | string | Directory identifier. |
| `directReportCount` | number | Number of direct reports. |
| `displayName` | string | Person display name. |
| `email` | string | Email address. |
| `firstName` | string | First name. |
| `id` | string | Unique person identifier. |
| `isTeamLeader` | boolean | Whether the person has direct reports. |
| `lastName` | string | Last name. |
| `officialPictureUrl` | string | Official profile picture URL. |
| `pictureUrl` | string | Profile picture URL. |
| `reportingPath` | array<string> | Hierarchy path of leader ids. |
| `teamLeaderId` | string | Direct leader person identifier. |
| `title` | string | Job title. |
| `totalReportCount` | number | Total direct and indirect reports. |

## Native endpoint

Through the native JustSift API, this operation is `GET /people/:idOrEmail` (base URL `https://api.justsift.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.

