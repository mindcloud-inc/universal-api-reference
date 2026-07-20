# Maildroppa: Delete Subscriber Field By ID



```
DELETE https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/delete-subscriber-field-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildroppa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/delete-subscriber-field-by-id?connectionId=$CONNECTION_ID&fieldTypeId=string&subscriberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fieldTypeId": "string",
  "subscriberId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/delete-subscriber-field-by-id?${params}`, {
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
| `fieldTypeId` | string | yes |  |
| `subscriberId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | True when delete subscriber field by id completed. |

## Native endpoint

Through the native Maildroppa API, this operation is `DELETE /subscribers/fields/by-id/{subscriberId}/{fieldTypeId}` (base URL `https://api.maildroppa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-subscriber-field-by-id.md) for the provider-specific parameters and requirements.

