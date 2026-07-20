# Hygraph: Publish Asset

Publishes an asset to content stages in Hygraph.

```
PUT https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/publish-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hygraph `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/publish-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/publish-asset', {
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
| `variables` | object | yes | Required variables: id. Optional: to. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "publishAsset": {
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
| `data.publishAsset` | object | Published asset returned by Hygraph. |
| `data.publishAsset.id` | string | Published asset ID. |
| `data.publishAsset.stage` | string | Published asset stage. |
| `extensions` | object | Optional GraphQL response extensions. |

## Native endpoint

Through the native Hygraph API, this operation is `POST` (base URL `{{credentials.endpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-asset.md) for the provider-specific parameters and requirements.

