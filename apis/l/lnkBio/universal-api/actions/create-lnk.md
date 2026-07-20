# Lnk.Bio: Create Lnk

Creates a new Lnk in Lnk.Bio.

```
POST https://connect.mindcloud.co/v1/universal/lnkBio/latest/actions/create-lnk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lnk.Bio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lnkBio/latest/actions/create-lnk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "link": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lnkBio/latest/actions/create-lnk', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "link": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | The title shown for the Lnk on your public Lnk.Bio profile. |
| `link` | string | yes | The destination URL for the new Lnk. |
| `image` | string | no | Optional image URL for the Lnk. |
| `groupId` | number | no | Optional Lnk.Bio group identifier for the new Lnk. |
| `scheduleFrom` | string | no | Optional RFC3339 timestamp for when the Lnk should become active. |
| `scheduleTo` | string | no | Optional RFC3339 timestamp for when the Lnk should stop being active. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": 1,
        "url": "https://example.com"
      },
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
| `data.id` | number | The identifier of the created Lnk. |
| `data.url` | string | The public Lnk.Bio profile URL. |
| `errors` | array<string> | Errors returned by the Lnk.Bio API. |
| `status` | boolean | Whether the create Lnk request succeeded. |

## Native endpoint

Through the native Lnk.Bio API, this operation is `POST /lnk/add` (base URL `https://lnk.bio/oauth/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lnk.md) for the provider-specific parameters and requirements.

