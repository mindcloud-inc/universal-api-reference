# BASIC: Delete specific settings values

Deletes specific project setting values from BASIC.

```
DELETE https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/delete-specific-settings-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/delete-specific-settings-values?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/delete-specific-settings-values?${params}`, {
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
      "data": {
        "auth": {
          "redirect_uris": [
            [
              "string"
            ]
          ]
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.auth.redirect_uris[]` | array<string> |  |

## Native endpoint

Through the native BASIC API, this operation is `DELETE /project/{id}/settings` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-specific-settings-values.md) for the provider-specific parameters and requirements.

