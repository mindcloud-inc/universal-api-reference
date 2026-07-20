# Draftable: Delete Comparison

Deletes a document comparison from Draftable.

```
DELETE https://connect.mindcloud.co/v1/universal/draftable/latest/actions/delete-comparison
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Draftable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/draftable/latest/actions/delete-comparison?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/draftable/latest/actions/delete-comparison?${params}`, {
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
| `identifier` | string | yes | The comparison identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "identifier": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `identifier` | string |  |

## Native endpoint

Through the native Draftable API, this operation is `DELETE /comparisons/{{identifier}}` (base URL `https://api.draftable.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-comparison.md) for the provider-specific parameters and requirements.

