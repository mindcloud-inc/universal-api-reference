# Hygraph: Delete Asset

Deletes an existing asset from Hygraph.

```
DELETE https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/delete-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hygraph `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/delete-asset?connectionId=$CONNECTION_ID&variables=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/delete-asset?${params}`, {
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
| `variables` | object | yes | Required variables: id. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "deleteAsset": {
          "id": "string"
        }
      },
      "extensions": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.deleteAsset` | object | Deleted asset returned by Hygraph. |
| `data.deleteAsset.id` | string | Deleted asset ID. |
| `extensions` | object | Optional GraphQL response extensions. |

## Native endpoint

Through the native Hygraph API, this operation is `POST` (base URL `{{credentials.endpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-asset.md) for the provider-specific parameters and requirements.

