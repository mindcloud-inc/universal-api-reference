# GrowthBook: Deletes a single attribute

Deletes an existing attribute from GrowthBook.

```
DELETE https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/delete-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/delete-attribute?connectionId=$CONNECTION_ID&property=sampleAttribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "property": "sampleAttribute"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/delete-attribute?${params}`, {
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
| `property` | string | yes | The attribute property Default: `sampleAttribute`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedProperty": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedProperty` | string |  |

## Native endpoint

Through the native GrowthBook API, this operation is `DELETE /attributes/:property` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-attribute.md) for the provider-specific parameters and requirements.

