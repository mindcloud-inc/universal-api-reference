# Pipedream Utils: Add Files To /tmp

Adds files to /tmp in Pipedream Utils.

```
POST https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/add-files-to-tmp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream Utils `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/add-files-to-tmp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "files[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/add-files-to-tmp', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "files[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `files[]` | array<string> | yes | An array of file URLs or base64-encoded file contents |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "filename": "Ava Chen",
          "filepath": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].filename` | string |  |
| `[].filepath` | string |  |

## Native endpoint

Through the native Pipedream Utils API, this operation is `GET` (base URL `https://pipedream.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-files-to-tmp.md) for the provider-specific parameters and requirements.

