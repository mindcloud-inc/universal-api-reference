# Stormboard: List Storms

Retrieves your Storms from Stormboard.

```
GET https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/list-storms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stormboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/list-storms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/list-storms?${params}`, {
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
| `folderId` | number | no | Filter storms by dashboard folder ID. |
| `needle` | string | no | Filter storms by storm title text. |
| `order` | string | no | Order by activity, alpha, frequency, or starred. |
| `results` | number | no | Maximum number of storms to return. |
| `start` | number | no | Start the result list at this index. |
| `status` | string | no | Filter by storm status: open or closed. |
| `teamId` | number | no | Filter storms by team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasmore": true,
      "status": 1,
      "storms": [
        {
          "admin": 1,
          "bg": "string",
          "canDelete": "string",
          "closed": true,
          "favorite": 1,
          "guestPass": true,
          "id": 1,
          "palette": "string",
          "plan": {
            "custom": 1
          },
          "showactivity": 1,
          "status": 1,
          "title": "string",
          "type": "string",
          "userId": 1
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
| `hasmore` | boolean |  |
| `status` | number |  |
| `storms` | array<object> |  |
| `storms[].admin` | number |  |
| `storms[].bg` | string |  |
| `storms[].canDelete` | string |  |
| `storms[].closed` | boolean |  |
| `storms[].favorite` | number |  |
| `storms[].guestPass` | boolean |  |
| `storms[].id` | number |  |
| `storms[].palette` | string |  |
| `storms[].plan` | object |  |
| `storms[].plan.custom` | number |  |
| `storms[].showactivity` | number |  |
| `storms[].status` | number |  |
| `storms[].title` | string |  |
| `storms[].type` | string |  |
| `storms[].userId` | number |  |

## Native endpoint

Through the native Stormboard API, this operation is `GET /storms/list` (base URL `https://api.stormboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-storms.md) for the provider-specific parameters and requirements.

