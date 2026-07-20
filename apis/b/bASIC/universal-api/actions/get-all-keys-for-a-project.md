# BASIC: Get all keys for a project

Retrieves project API keys from BASIC.

```
GET https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-all-keys-for-a-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-all-keys-for-a-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-all-keys-for-a-project?${params}`, {
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
      "data": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "is_private": true,
          "label": "string",
          "last_used": "2026-05-07T12:00:00.000Z",
          "roles": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].created_at` | date |  |
| `data[].id` | string |  |
| `data[].is_private` | boolean |  |
| `data[].label` | string |  |
| `data[].last_used` | date |  |
| `data[].roles` | string |  |

## Native endpoint

Through the native BASIC API, this operation is `GET /project/{id}/key` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-keys-for-a-project.md) for the provider-specific parameters and requirements.

