# Hygraph: Unpublish Asset

Unpublishes an asset from content stages in Hygraph.

```
PUT https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/unpublish-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hygraph `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/unpublish-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/unpublish-asset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | yes | Required variables: id. Optional: from, to. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "unpublishAsset": {
          "id": "string",
          "stage": "string"
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
| `data.unpublishAsset` | object | Unpublished asset returned by Hygraph. |
| `data.unpublishAsset.id` | string | Unpublished asset ID. |
| `data.unpublishAsset.stage` | string | Unpublished asset stage. |
| `extensions` | object | Optional GraphQL response extensions. |

## Native endpoint

Through the native Hygraph API, this operation is `POST` (base URL `{{credentials.endpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unpublish-asset.md) for the provider-specific parameters and requirements.

