# ThingsBoard: Get Asset Info

Retrieves asset info from ThingsBoard.

```
GET https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-asset-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThingsBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-asset-info?connectionId=$CONNECTION_ID&assetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-asset-info?${params}`, {
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
| `assetId` | string | yes | The ThingsBoard asset ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assetProfileId": {
        "id": "string"
      },
      "createdTime": 1,
      "id": {
        "entityType": "string",
        "id": "string"
      },
      "label": "string",
      "name": "Ava Chen",
      "ownerName": "Ava Chen",
      "tenantId": {
        "id": "string"
      },
      "type": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assetProfileId.id` | string |  |
| `createdTime` | number |  |
| `id.entityType` | string |  |
| `id.id` | string |  |
| `label` | string |  |
| `name` | string |  |
| `ownerName` | string |  |
| `tenantId.id` | string |  |
| `type` | string |  |
| `version` | number |  |

## Native endpoint

Through the native ThingsBoard API, this operation is `GET /asset/info/:assetId` (base URL `{{credentials.baseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset-info.md) for the provider-specific parameters and requirements.

