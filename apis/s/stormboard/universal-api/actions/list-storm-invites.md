# Stormboard: List Storm Invites

Retrieves your Storm invites from Stormboard.

```
GET https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/list-storm-invites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stormboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/list-storm-invites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/list-storm-invites?${params}`, {
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
| `needle` | string | no | Filter invites by storm title text. |
| `teamId` | number | no | Filter invites by team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1,
      "storms": [
        {
          "activity": 1,
          "admin": 1,
          "bg": "string",
          "closed": true,
          "favorite": 1,
          "id": 1,
          "palette": "string",
          "team": {
            "id": 1
          },
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
| `status` | number |  |
| `storms` | array<object> |  |
| `storms[].activity` | number |  |
| `storms[].admin` | number |  |
| `storms[].bg` | string |  |
| `storms[].closed` | boolean |  |
| `storms[].favorite` | number |  |
| `storms[].id` | number |  |
| `storms[].palette` | string |  |
| `storms[].team` | object |  |
| `storms[].team.id` | number |  |
| `storms[].title` | string |  |
| `storms[].type` | string |  |
| `storms[].userId` | number |  |

## Native endpoint

Through the native Stormboard API, this operation is `GET /storms/invites` (base URL `https://api.stormboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-storm-invites.md) for the provider-specific parameters and requirements.

