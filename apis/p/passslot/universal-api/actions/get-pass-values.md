# Passslot: Get Pass Values



```
GET https://connect.mindcloud.co/v1/universal/passslot/latest/actions/get-pass-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Passslot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passslot/latest/actions/get-pass-values?connectionId=$CONNECTION_ID&passTypeIdentifier=string&serialNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "passTypeIdentifier": "string",
  "serialNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passslot/latest/actions/get-pass-values?${params}`, {
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
| `passTypeIdentifier` | string | yes | Passslot pass type identifier. |
| `serialNumber` | string | yes | Pass serial number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "serialNumber": "string",
      "values": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `serialNumber` | string | Pass serial number. |
| `values` | object | Resolved pass values. |

## Native endpoint

Through the native Passslot API, this operation is `GET passes/:passTypeIdentifier/:serialNumber/values` (base URL `https://api.passslot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pass-values.md) for the provider-specific parameters and requirements.

