# Freshsales Classic: List Lifecycle Stages

Retrieves lifecycle stages from Freshsales Classic.

```
GET https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-lifecycle-stages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshsales Classic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-lifecycle-stages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-lifecycle-stages?${params}`, {
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
      "contactStatusIds": [
        1
      ],
      "default": true,
      "disabled": true,
      "id": 1,
      "name": "Ava Chen",
      "position": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactStatusIds` | array<number> | Related contact status IDs. |
| `default` | boolean | Whether the stage is a default stage. |
| `disabled` | boolean | Whether the stage is disabled. |
| `id` | number | Lifecycle stage ID. |
| `name` | string | Lifecycle stage name. |
| `position` | number | Lifecycle stage position. |
| `type` | string | Lifecycle stage type. |

## Native endpoint

Through the native Freshsales Classic API, this operation is `GET /selector/lifecycle_stages` (base URL `https://{{credentials.bundleAlias}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lifecycle-stages.md) for the provider-specific parameters and requirements.

