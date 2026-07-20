# GrowthBook: Delete a single customField

Deletes an existing custom field from GrowthBook.

```
DELETE https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/delete-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/delete-custom-field?connectionId=$CONNECTION_ID&id=prj_19g6smo332up7" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "prj_19g6smo332up7"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/delete-custom-field?${params}`, {
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
| `id` | string | yes | Default: `prj_19g6smo332up7`. |
| `index` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedId` | string |  |

## Native endpoint

Through the native GrowthBook API, this operation is `DELETE /custom-fields/:id` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-custom-field.md) for the provider-specific parameters and requirements.

