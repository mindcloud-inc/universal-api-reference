# Atlar: Delete facility activity

Deletes an existing facility activity from Atlar.

```
DELETE https://connect.mindcloud.co/v1/universal/atlar/latest/actions/delete-facility-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/delete-facility-activity?connectionId=$CONNECTION_ID&id=string&activityId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "activityId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlar/latest/actions/delete-facility-activity?${params}`, {
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
| `id` | string<string> | yes |  |
| `activityId` | string<string> | yes |  |
| `If_Match` | string<string> | no |  |

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
| `id` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Atlar API, this operation is `DELETE /financial-data/v2beta/facilities/{id}/activities/{activityId}` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-facility-activity.md) for the provider-specific parameters and requirements.

