# e-Gov: List Dataset Relationships

Retrieves a dataset's relationships from e-Gov.

```
GET https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-dataset-relationships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-dataset-relationships?connectionId=$CONNECTION_ID&id=moj_20180907_0008" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "moj_20180907_0008"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-dataset-relationships?${params}`, {
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
| `id` | string | yes | Default: `moj_20180907_0008`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id2` | string | no |  |
| `rel` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native e-Gov API returns.

## Native endpoint

Through the native e-Gov API, this operation is `GET /package_relationships_list` (base URL `https://data.e-gov.go.jp/data/api/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dataset-relationships.md) for the provider-specific parameters and requirements.

