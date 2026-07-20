# Starburst Galaxy: Get data product



```
GET https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-data-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starburst Galaxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-data-product?connectionId=$CONNECTION_ID&dataProductId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataProductId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-data-product?${params}`, {
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
| `dataProductId` | string | yes | Starburst Galaxy data product ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "2026-05-07T12:00:00.000Z",
      "dataProductId": "string",
      "defaultClusterId": "string",
      "description": "string",
      "modifiedOn": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "schemaName": "Ava Chen",
      "summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | date |  |
| `dataProductId` | string |  |
| `defaultClusterId` | string |  |
| `description` | string |  |
| `modifiedOn` | date |  |
| `name` | string |  |
| `schemaName` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native Starburst Galaxy API, this operation is `GET /public/api/v1/dataProduct/{dataProductId}` (base URL `https://mindcloud.galaxy.starburst.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-product.md) for the provider-specific parameters and requirements.

