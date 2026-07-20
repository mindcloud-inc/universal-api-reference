# Neon: List project snapshots

Retrieves project snapshots from Neon.

```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/list-snapshots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/list-snapshots?connectionId=$CONNECTION_ID&project_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/list-snapshots?${params}`, {
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
| `project_id` | string | yes | Neon API parameter project_id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "snapshots": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `snapshots` | array<object> |  |

## Native endpoint

Through the native Neon API, this operation is `GET /projects/:project_id/snapshots` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-snapshots.md) for the provider-specific parameters and requirements.

