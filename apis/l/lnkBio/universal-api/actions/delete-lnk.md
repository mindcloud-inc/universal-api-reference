# Lnk.Bio: Delete Lnk

Deletes an existing Lnk from Lnk.Bio.

```
DELETE https://connect.mindcloud.co/v1/universal/lnkBio/latest/actions/delete-lnk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lnk.Bio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/lnkBio/latest/actions/delete-lnk?connectionId=$CONNECTION_ID&linkId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lnkBio/latest/actions/delete-lnk?${params}`, {
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
| `linkId` | number | yes | The identifier of the Lnk to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> | Errors returned by the Lnk.Bio API. |
| `status` | boolean | Whether the delete Lnk request succeeded. |

## Native endpoint

Through the native Lnk.Bio API, this operation is `POST /lnk/delete` (base URL `https://lnk.bio/oauth/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-lnk.md) for the provider-specific parameters and requirements.

