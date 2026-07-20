# OneSignal: Remove Alias

Removes a user alias from OneSignal.

```
DELETE https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/remove-alias
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/remove-alias?connectionId=$CONNECTION_ID&aliasId=string&aliasLabel=string&aliasLabelToDelete=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "aliasId": "string",
  "aliasLabel": "string",
  "aliasLabelToDelete": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/remove-alias?${params}`, {
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
| `aliasId` | string | yes | The alias value for the selected alias label. |
| `aliasLabel` | string | yes | The alias namespace to look up, such as external_id. |
| `aliasLabelToDelete` | string | yes | The alias namespace to remove from the user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "identity": {
        "externalId": "string",
        "onesignalId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `identity.externalId` | string |  |
| `identity.onesignalId` | string |  |

## Native endpoint

Through the native OneSignal API, this operation is `DELETE /apps/:app_id/users/by/:alias_label/:alias_id/identity/:alias_label_to_delete` (base URL `https://api.onesignal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-alias.md) for the provider-specific parameters and requirements.

