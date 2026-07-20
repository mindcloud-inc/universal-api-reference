# Rithum DSCO: Delete Assortment

Deletes an assortment from Rithum DSCO.

```
DELETE https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/delete-assortment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum DSCO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/delete-assortment?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/delete-assortment?${params}`, {
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
| `id` | string | yes | Required DSCO assortment ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Deleted assortment ID. |
| `success` | boolean | Whether the delete request succeeded. |

## Native endpoint

Through the native Rithum DSCO API, this operation is `DELETE assortment/:id` (base URL `https://api.dsco.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-assortment.md) for the provider-specific parameters and requirements.

