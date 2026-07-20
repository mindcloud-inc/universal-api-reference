# Linkbreakers: Create Multiple Links

Creates multiple new links in Linkbreakers.

```
POST https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/create-multiple-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkbreakers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/create-multiple-links" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "links[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/create-multiple-links', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "links[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `links[]` | array<object> | yes | Links to create in one batch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": [
        {
          "createdAt": "https://example.com",
          "destination": "https://example.com",
          "directoryId": "https://example.com",
          "entrypoint": "https://example.com",
          "eventCount": 1,
          "id": "https://example.com",
          "metadata": {},
          "name": "https://example.com",
          "shortlink": "https://example.com",
          "updatedAt": "https://example.com",
          "workspaceId": "https://example.com"
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
| `links` | array<object> | Batch-created links. |
| `links[].createdAt` | string |  |
| `links[].destination` | string |  |
| `links[].directoryId` | string |  |
| `links[].entrypoint` | string |  |
| `links[].eventCount` | number |  |
| `links[].id` | string |  |
| `links[].metadata` | object |  |
| `links[].name` | string |  |
| `links[].shortlink` | string |  |
| `links[].updatedAt` | string |  |
| `links[].workspaceId` | string |  |

## Native endpoint

Through the native Linkbreakers API, this operation is `POST /v1/links/bulk` (base URL `https://api.linkbreakers.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-multiple-links.md) for the provider-specific parameters and requirements.

