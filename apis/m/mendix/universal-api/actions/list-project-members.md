# Mendix: List Project Members

Retrieves project team members from Mendix.

```
GET https://connect.mindcloud.co/v1/universal/mendix/latest/actions/list-project-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendix/latest/actions/list-project-members?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=d92064a5-b1fd-4be4-97db-53fc90201d1c" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "d92064a5-b1fd-4be4-97db-53fc90201d1c"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendix/latest/actions/list-project-members?${params}`, {
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
| `projectId` | string | yes | The unique identifier of a project. Example: `d92064a5-b1fd-4be4-97db-53fc90201d1c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "avatarUrl": "https://example.com",
          "company": {
            "companyName": "Ava Chen"
          },
          "displayName": "Ava Chen",
          "isActive": true,
          "userId": "string"
        }
      ],
      "page": {
        "elements": 1,
        "offset": 1,
        "totalElements": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].avatarUrl` | string | Avatar image URL of the member. |
| `items[].company.companyName` | string | Name of the company to which the member belongs. |
| `items[].displayName` | string | Full name of the member. |
| `items[].isActive` | boolean | Indicates whether the member is active on the platform. |
| `items[].userId` | string | Unique identifier for the member on the Mendix platform. |
| `page.elements` | number | Number of elements returned. |
| `page.offset` | number | Pagination offset. |
| `page.totalElements` | number | Total number of matching project members. |

## Native endpoint

Through the native Mendix API, this operation is `GET /projects/:projectId/members` (base URL `https://projects-api.home.mendix.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-members.md) for the provider-specific parameters and requirements.

