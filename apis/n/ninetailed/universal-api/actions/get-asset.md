# Ninetailed: Get Asset



```
GET https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/get-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninetailed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/get-asset?connectionId=$CONNECTION_ID&spaceId=string&environmentId=string&assetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "string",
  "environmentId": "string",
  "assetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/get-asset?${params}`, {
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
| `spaceId` | string | yes | Contentful space ID. |
| `environmentId` | string | yes | Contentful environment ID. |
| `assetId` | string | yes | Contentful asset ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": {},
      "metadata": {},
      "sys": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | object |  |
| `metadata` | object |  |
| `sys` | object |  |

## Native endpoint

Through the native Ninetailed API, this operation is `GET /spaces/:space_id/environments/:environment_id/assets/:asset_id` (base URL `https://api.contentful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset.md) for the provider-specific parameters and requirements.

