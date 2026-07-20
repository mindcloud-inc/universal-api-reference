# Raklet: Create Post



```
POST https://connect.mindcloud.co/v1/universal/raklet/latest/actions/create-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raklet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/raklet/latest/actions/create-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/raklet/latest/actions/create-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject` | string | yes |  |
| `description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Comment": 1,
      "CreatedOn": "2026-05-07T12:00:00.000Z",
      "Description": "string",
      "Id": "string",
      "IsPinned": true,
      "Like": 1,
      "PermissionType": 1,
      "PermissionTypeText": "string",
      "PublishedOn": "2026-05-07T12:00:00.000Z",
      "Share": 1,
      "ShortDescription": "string",
      "Slug": "string",
      "Status": 1,
      "StatusText": "string",
      "Subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Comment` | number |  |
| `CreatedOn` | date |  |
| `Description` | string |  |
| `Id` | string |  |
| `IsPinned` | boolean |  |
| `Like` | number |  |
| `PermissionType` | number |  |
| `PermissionTypeText` | string |  |
| `PublishedOn` | date |  |
| `Share` | number |  |
| `ShortDescription` | string |  |
| `Slug` | string |  |
| `Status` | number |  |
| `StatusText` | string |  |
| `Subject` | string |  |

## Native endpoint

Through the native Raklet API, this operation is `POST /organisations/:organisationId/posts` (base URL `https://api.raklet.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-post.md) for the provider-specific parameters and requirements.

