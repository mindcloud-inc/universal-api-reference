# Dart: Get User Space Configuration

Retrieves user space configuration details from Dart.

```
GET https://connect.mindcloud.co/v1/universal/dart/latest/actions/get-user-space-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dart/latest/actions/get-user-space-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dart/latest/actions/get-user-space-configuration?${params}`, {
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
      "assignees": [
        {
          "email": "ava@example.com",
          "name": "Ava Chen"
        }
      ],
      "dartboards": [
        "string"
      ],
      "folders": [
        "string"
      ],
      "priorities": [
        "string"
      ],
      "sizes": [
        "string"
      ],
      "skills": [
        "string"
      ],
      "statuses": [
        "string"
      ],
      "tags": [
        "string"
      ],
      "today": "2026-05-07T12:00:00.000Z",
      "types": [
        "string"
      ],
      "user": {
        "email": "ava@example.com",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignees[].email` | string |  |
| `assignees[].name` | string |  |
| `dartboards[]` | string |  |
| `folders[]` | string |  |
| `priorities[]` | string |  |
| `sizes[]` | string |  |
| `skills[]` | string |  |
| `statuses[]` | string |  |
| `tags[]` | string |  |
| `today` | date |  |
| `types[]` | string |  |
| `user.email` | string |  |
| `user.name` | string |  |

## Native endpoint

Through the native Dart API, this operation is `GET /config` (base URL `https://app.dartai.com/api/v0/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-space-configuration.md) for the provider-specific parameters and requirements.

