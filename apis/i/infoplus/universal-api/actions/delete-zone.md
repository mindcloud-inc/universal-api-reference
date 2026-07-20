# Infoplus: Delete Zone

Deletes an existing zone from Infoplus.

```
DELETE https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/delete-zone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infoplus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/delete-zone?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/delete-zone?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Deleted record ID. |

## Native endpoint

Through the native Infoplus API, this operation is `DELETE /zone/{zoneId}` (base URL `https://luxomo.infopluswms.com/infoplus-wms/api/v3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-zone.md) for the provider-specific parameters and requirements.

