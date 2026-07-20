# Chroma Cloud: Detach function

Detaches a function from a collection in Chroma Cloud.

```
DELETE https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/detach-function
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chroma Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/detach-function?connectionId=$CONNECTION_ID&collectionId=string&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string",
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/detach-function?${params}`, {
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
| `collectionId` | string | yes | Collection UUID. |
| `name` | string | yes | Attached function name. |
| `deleteOutput` | boolean | no | Whether to delete the output collection as well. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Chroma Cloud API, this operation is `POST /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/attached_functions/:name/detach` (base URL `https://api.trychroma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detach-function.md) for the provider-specific parameters and requirements.

