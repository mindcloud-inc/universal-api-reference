# GetResponse: List Websites

Retrieves a list of websites from GetResponse.

```
GET https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/list-websites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetResponse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/list-websites?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/list-websites?${params}`, {
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
| `name` | string | no | Filter websites by name |
| `status` | string | no | Filter websites by status |
| `statsFrom` | string | no | Filter website statistics start date |
| `statsTo` | string | no | Filter website statistics end date |
| `sortName` | string | no | Sort websites by name |
| `sortCreatedAt` | string | no | Sort websites by creation date |
| `sortUpdatedAt` | string | no | Sort websites by update date |
| `sortPageViews` | string | no | Sort websites by page views |
| `sortVisits` | string | no | Sort websites by visits |
| `sortUniqueVisitors` | string | no | Sort websites by unique visitors |
| `fields` | string | no | Comma-separated list of fields to return |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "status": "string",
      "websiteId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `status` | string |  |
| `websiteId` | string |  |

## Native endpoint

Through the native GetResponse API, this operation is `GET /websites` (base URL `https://api.getresponse.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-websites.md) for the provider-specific parameters and requirements.

