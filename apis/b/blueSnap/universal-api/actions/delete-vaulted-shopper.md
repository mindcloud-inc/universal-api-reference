# BlueSnap: Delete Vaulted Shopper

Deletes a vaulted shopper from BlueSnap.

```
DELETE https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/delete-vaulted-shopper
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueSnap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/delete-vaulted-shopper?connectionId=$CONNECTION_ID&vaultedShopperId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vaultedShopperId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/delete-vaulted-shopper?${params}`, {
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
| `vaultedShopperId` | string | yes | ID of the vaulted shopper to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Delete request status message. |

## Native endpoint

Through the native BlueSnap API, this operation is `DELETE /vaulted-shoppers/:vaultedShopperId` (base URL `https://sandbox.bluesnap.com/services/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-vaulted-shopper.md) for the provider-specific parameters and requirements.

