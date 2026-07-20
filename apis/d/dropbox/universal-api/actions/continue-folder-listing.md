# Dropbox: Continue Folder Listing

Retrieves more Dropbox folder contents using a cursor.

```
GET https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/continue-folder-listing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/continue-folder-listing?connectionId=$CONNECTION_ID&cursor=ZtkX9_EHj3x7PMkVuFIhwKYXEpwpLwyxp9vMKomUhllil9q7eWiAu" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cursor": "ZtkX9_EHj3x7PMkVuFIhwKYXEpwpLwyxp9vMKomUhllil9q7eWiAu"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/continue-folder-listing?${params}`, {
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
| `cursor` | string | yes | The cursor returned by a previous folder listing call. Example: `ZtkX9_EHj3x7PMkVuFIhwKYXEpwpLwyxp9vMKomUhllil9q7eWiAu`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "hasMore": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursor` | string |  |
| `hasMore` | boolean |  |

## Native endpoint

Through the native Dropbox API, this operation is `POST /files/list_folder/continue` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/continue-folder-listing.md) for the provider-specific parameters and requirements.

