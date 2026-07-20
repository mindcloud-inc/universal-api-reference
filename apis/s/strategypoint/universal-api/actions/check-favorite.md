# Strategypoint: Check Favorite

Checks favorites in Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/check-favorite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/check-favorite?connectionId=$CONNECTION_ID&object=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "object": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/check-favorite?${params}`, {
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
| `layoutId` | number | no | The layout identifier to check. |
| `object` | string | yes | The object type to check for a favorite entry. |
| `objectId` | number | no | The object identifier to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "favorite": true,
      "object": "string",
      "objectId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `favorite` | boolean | Whether the target is marked as a favorite. |
| `object` | string | The related object type. |
| `objectId` | number | The related object identifier. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /favorites` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-favorite.md) for the provider-specific parameters and requirements.

