# RD Station Marketing: Delete Custom Field



```
DELETE https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/delete-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station Marketing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/delete-custom-field?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/delete-custom-field?${params}`, {
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
| `uuid` | string | yes | Contact field UUID in path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | The raw response body. The saved successful response was an empty string (HTTP 204). |

## Native endpoint

Through the native RD Station Marketing API, this operation is `DELETE /platform/contacts/fields/:uuid` (base URL `https://api.rd.services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-custom-field.md) for the provider-specific parameters and requirements.

