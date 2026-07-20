# Passslot: List Passes



```
GET https://connect.mindcloud.co/v1/universal/passslot/latest/actions/list-passes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Passslot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passslot/latest/actions/list-passes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passslot/latest/actions/list-passes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "passTypeIdentifier": "string",
      "serialNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `passTypeIdentifier` | string | Pass type identifier. |
| `serialNumber` | string | Pass serial number. |

## Native endpoint

Through the native Passslot API, this operation is `GET passes` (base URL `https://api.passslot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-passes.md) for the provider-specific parameters and requirements.

