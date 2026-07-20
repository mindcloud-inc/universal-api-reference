# Farmbrite: Delete plot

Deletes an existing plot from Farmbrite.

```
DELETE https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/delete-plot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/delete-plot?connectionId=$CONNECTION_ID&plotId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "plotId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/delete-plot?${params}`, {
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
| `plotId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | string |  |

## Native endpoint

Through the native Farmbrite API, this operation is `DELETE /plots/:plot_id` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-plot.md) for the provider-specific parameters and requirements.

