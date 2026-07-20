# Canva: List Designs

Retrieves designs from the current Canva user's projects.

```
GET https://connect.mindcloud.co/v1/universal/canva/latest/actions/list-designs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canva `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canva/latest/actions/list-designs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/canva/latest/actions/list-designs?${params}`, {
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
| `query` | string | no | Search term used to filter the user's designs. |
| `ownership` | list | no | Filter designs by whether they are owned by or shared with the user. One of: `any`, `owned`, `shared`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `continuation` | string | no | Continuation token returned by a previous List Designs call. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "createdAt": 1,
          "id": "string",
          "owner": {
            "teamId": "string",
            "userId": "string"
          },
          "pageCount": 1,
          "title": "string",
          "updatedAt": 1,
          "urls": {
            "editUrl": "https://example.com",
            "viewUrl": "https://example.com"
          }
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
| `items` | array<object> |  |
| `items[].createdAt` | number |  |
| `items[].id` | string |  |
| `items[].owner` | object |  |
| `items[].owner.teamId` | string |  |
| `items[].owner.userId` | string |  |
| `items[].pageCount` | number |  |
| `items[].title` | string |  |
| `items[].updatedAt` | number |  |
| `items[].urls` | object |  |
| `items[].urls.editUrl` | string |  |
| `items[].urls.viewUrl` | string |  |

## Native endpoint

Through the native Canva API, this operation is `GET /v1/designs` (base URL `https://api.canva.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-designs.md) for the provider-specific parameters and requirements.

