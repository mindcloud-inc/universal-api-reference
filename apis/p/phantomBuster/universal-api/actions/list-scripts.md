# PhantomBuster: List Scripts

Retrieves scripts from PhantomBuster.

```
GET https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/list-scripts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhantomBuster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/list-scripts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/list-scripts?${params}`, {
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
| `branch` | string | no |  |
| `exclude` | list | no | One of: `modules`, `non-modules`. |
| `org` | string | no |  |
| `scriptIds` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": 1,
      "defaultBranch": "string",
      "id": "string",
      "name": "Ava Chen",
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number |  |
| `defaultBranch` | string |  |
| `id` | string |  |
| `name` | string |  |
| `updated_at` | number |  |

## Native endpoint

Through the native PhantomBuster API, this operation is `GET /scripts/fetch-all` (base URL `https://api.phantombuster.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-scripts.md) for the provider-specific parameters and requirements.

