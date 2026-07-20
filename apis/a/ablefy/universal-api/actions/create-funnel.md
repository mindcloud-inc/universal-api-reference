# Ablefy: Create Funnel

Creates a new funnel in Ablefy.

```
POST https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/create-funnel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ablefy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/create-funnel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "funnelNodeAttributes": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/create-funnel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "funnelNodeAttributes": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `funnelNodeAttributes.contentPageId` | string | no | Required content_page_id |
| `funnelNodeAttributes.form` | list<string> | no | Funnel node form One of: `node_link`, `node_page`. |
| `funnelNodeAttributes.redirectionUrl` | string | no | Redirection url if type is link |
| `name` | string | no |  |
| `funnelNodeAttributes` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "applied": 1,
        "copyFromId": {},
        "createdAt": "2026-05-07T12:00:00.000Z",
        "funnelNodeId": 1,
        "id": 1,
        "name": "Ava Chen",
        "sellerId": 1,
        "sharingId": {},
        "sharingItemId": {},
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.applied` | number |  |
| `data.copyFromId` | object |  |
| `data.createdAt` | date |  |
| `data.funnelNodeId` | number |  |
| `data.id` | number |  |
| `data.name` | string |  |
| `data.sellerId` | number |  |
| `data.sharingId` | object |  |
| `data.sharingItemId` | object |  |
| `data.updatedAt` | date |  |
| `success` | boolean |  |

## Native endpoint

Through the native Ablefy API, this operation is `POST /api/funnels` (base URL `https://api.myablefy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-funnel.md) for the provider-specific parameters and requirements.

