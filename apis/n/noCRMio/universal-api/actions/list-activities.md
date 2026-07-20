# noCRM.io: List Activities

Retrieves activities from noCRM.io.

```
GET https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a noCRM.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-activities?${params}`, {
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
      "color": "string",
      "icon": "string",
      "id": 1,
      "isDisabled": true,
      "kind": "string",
      "name": "Ava Chen",
      "parentId": "string",
      "position": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `icon` | string |  |
| `id` | number |  |
| `isDisabled` | boolean |  |
| `kind` | string |  |
| `name` | string |  |
| `parentId` | string |  |
| `position` | string |  |

## Native endpoint

Through the native noCRM.io API, this operation is `GET /activities` (base URL `{{credentials.baseUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-activities.md) for the provider-specific parameters and requirements.

