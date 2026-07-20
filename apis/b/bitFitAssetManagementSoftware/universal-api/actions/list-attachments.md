# bitFit Asset Management Software: List Attachments



```
GET https://connect.mindcloud.co/v1/universal/bitFitAssetManagementSoftware/latest/actions/list-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a bitFit Asset Management Software `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitFitAssetManagementSoftware/latest/actions/list-attachments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitFitAssetManagementSoftware/latest/actions/list-attachments?${params}`, {
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
| `limit` | number | no | Maximum number of records to return. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `offset` | number | no | Number of records to skip before returning results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> | The list of matching BitFit attachments. |

## Native endpoint

Through the native bitFit Asset Management Software API, this operation is `GET /v2/attachments` (base URL `https://api-assets.bitfit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-attachments.md) for the provider-specific parameters and requirements.

