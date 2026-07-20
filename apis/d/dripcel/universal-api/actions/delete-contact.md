# Dripcel: Delete Contact

Deletes a contact from Dripcel by cell number.

```
DELETE https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/delete-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dripcel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/delete-contact?connectionId=$CONNECTION_ID&cell=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cell": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/delete-contact?${params}`, {
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
| `cell` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "acknowledged": true,
        "deletedCount": 1
      },
      "ok": true,
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.acknowledged` | boolean |  |
| `data.deletedCount` | number |  |
| `ok` | boolean |  |
| `requestId` | string |  |

## Native endpoint

Through the native Dripcel API, this operation is `DELETE /contacts/:cell` (base URL `https://api.dripcel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact.md) for the provider-specific parameters and requirements.

