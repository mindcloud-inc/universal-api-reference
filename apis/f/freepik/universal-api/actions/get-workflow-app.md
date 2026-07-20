# Freepik: Get Workflow App



```
GET https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-workflow-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freepik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-workflow-app?connectionId=$CONNECTION_ID&appId=DXOpclpxKi" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "DXOpclpxKi"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-workflow-app?${params}`, {
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
| `appId` | string | yes | Freepik workflow app identifier. Default: `DXOpclpxKi`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "community_name": "Ava Chen",
      "description": "string",
      "estimated_cost_credits": 1,
      "inputs": [
        {}
      ],
      "name": "Ava Chen",
      "sqid": "string",
      "thumbnail_url": "https://example.com",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `community_name` | string | Community publisher name. |
| `description` | string | Workflow app description. |
| `estimated_cost_credits` | number | Estimated cost in credits. |
| `inputs` | array<object> | Workflow app inputs. |
| `name` | string | Workflow app name. |
| `sqid` | string | Workflow app identifier. |
| `thumbnail_url` | string | Thumbnail URL. |
| `visibility` | string | Workflow app visibility. |

## Native endpoint

Through the native Freepik API, this operation is `GET /v1/ai/apps/{{app-id}}` (base URL `https://api.freepik.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow-app.md) for the provider-specific parameters and requirements.

